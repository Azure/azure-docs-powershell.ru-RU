---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 22C6845E-D7BD-4BBC-B373-394A23488A94
online version: ''
schema: 2.0.0
ms.openlocfilehash: a0695dc42d9c540e30ddf9ac55bd6fc136c84bff
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075524"
---
# <span data-ttu-id="e80ff-101">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="e80ff-101">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span></span>

## <span data-ttu-id="e80ff-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e80ff-102">SYNOPSIS</span></span>
<span data-ttu-id="e80ff-103">Создание объекта конфигурации для обновления расписания резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="e80ff-103">Creates a backup schedule update configuration object.</span></span>

## <span data-ttu-id="e80ff-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e80ff-104">SYNTAX</span></span>

```
New-AzureStorSimpleDeviceBackupScheduleUpdateConfig -Id <String> -BackupType <String> -RecurrenceType <String>
 -RecurrenceValue <Int32> -RetentionCount <Int64> [-StartFromDateTime <String>] [-Enabled <Boolean>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e80ff-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e80ff-105">DESCRIPTION</span></span>
<span data-ttu-id="e80ff-106">Командлет **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** создает объект конфигурации **BackupScheduleUpdateRequest** .</span><span class="sxs-lookup"><span data-stu-id="e80ff-106">The **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** cmdlet creates a **BackupScheduleUpdateRequest** configuration object.</span></span>
<span data-ttu-id="e80ff-107">Используйте этот объект конфигурации для обновления политики резервного копирования с помощью командлета **Set-AzureStorSimpleDeviceBackupPolicy** .</span><span class="sxs-lookup"><span data-stu-id="e80ff-107">Use this configuration object to update a backup policy by using the **Set-AzureStorSimpleDeviceBackupPolicy** cmdlet.</span></span>

## <span data-ttu-id="e80ff-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e80ff-108">EXAMPLES</span></span>

### <span data-ttu-id="e80ff-109">Пример 1: Создание запроса на обновление расписания</span><span class="sxs-lookup"><span data-stu-id="e80ff-109">Example 1: Create a schedule update request</span></span>
```
PS C:\>New-AzureStorSimpleDeviceBackupScheduleUpdateConfig -Id "147f734d-a31a-4473-8501-6ba38be2cb30" -BackupType CloudSnapshot -RecurrenceType Hourly -RecurrenceValue 1 -RetentionCount 50 -Enabled $True
VERBOSE: ClientRequestId: ef346641-54b4-4273-8898-7f863e7c5b7e_PS


BackupType     : CloudSnapshot
Id             : 147f734d-a31a-4473-8501-6ba38be2cb30
Recurrence     : Microsoft.WindowsAzure.Management.StorSimple.Models.ScheduleRecurrence
RetentionCount : 50
StartTime      : 2014-12-16T00:39:32+05:30
Status         : Enabled
```

<span data-ttu-id="e80ff-110">Эта команда создает запрос на обновление расписания резервного копирования для расписания с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="e80ff-110">This command creates a backup schedule update request for the schedule that has the specified ID.</span></span>
<span data-ttu-id="e80ff-111">Запрос состоит в том, чтобы сделать расписание резервного копирования облачных снимков, которое будет повторяться каждый час.</span><span class="sxs-lookup"><span data-stu-id="e80ff-111">The request is to make the schedule a cloud snapshot backup that recurs every hour.</span></span>
<span data-ttu-id="e80ff-112">Резервные копии хранятся в течение 50 дней.</span><span class="sxs-lookup"><span data-stu-id="e80ff-112">The backups are kept for 50 days.</span></span>
<span data-ttu-id="e80ff-113">Это расписание включается по умолчанию, которое является текущим временем.</span><span class="sxs-lookup"><span data-stu-id="e80ff-113">This schedule is enabled from the default time, which is the current time.</span></span>

## <span data-ttu-id="e80ff-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e80ff-114">PARAMETERS</span></span>

### <span data-ttu-id="e80ff-115">-BackupType</span><span class="sxs-lookup"><span data-stu-id="e80ff-115">-BackupType</span></span>
<span data-ttu-id="e80ff-116">Указывает тип резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="e80ff-116">Specifies the backup type.</span></span>
<span data-ttu-id="e80ff-117">Допустимые значения: LocalSnapshot и CloudSnapshot.</span><span class="sxs-lookup"><span data-stu-id="e80ff-117">Valid values are: LocalSnapshot and CloudSnapshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e80ff-118">-Включено</span><span class="sxs-lookup"><span data-stu-id="e80ff-118">-Enabled</span></span>
<span data-ttu-id="e80ff-119">Указывает, следует ли включить расписание резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="e80ff-119">Indicates whether to enable the backup schedule.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e80ff-120">-ID</span><span class="sxs-lookup"><span data-stu-id="e80ff-120">-Id</span></span>
<span data-ttu-id="e80ff-121">Указывает ИД экземпляра расписания резервного копирования, которое требуется обновить.</span><span class="sxs-lookup"><span data-stu-id="e80ff-121">Specifies the instance ID of the backup schedule to update.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e80ff-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="e80ff-122">-Profile</span></span>
<span data-ttu-id="e80ff-123">Указывает профиль Azure.</span><span class="sxs-lookup"><span data-stu-id="e80ff-123">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="e80ff-124">-RecurrenceType</span><span class="sxs-lookup"><span data-stu-id="e80ff-124">-RecurrenceType</span></span>
<span data-ttu-id="e80ff-125">Указывает тип повторения для этого расписания резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="e80ff-125">Specifies the type of recurrence for this backup schedule.</span></span>
<span data-ttu-id="e80ff-126">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="e80ff-126">Valid values are:</span></span> 

- <span data-ttu-id="e80ff-127">Течение</span><span class="sxs-lookup"><span data-stu-id="e80ff-127">Minutes</span></span>
- <span data-ttu-id="e80ff-128">Почасовой</span><span class="sxs-lookup"><span data-stu-id="e80ff-128">Hourly</span></span>
- <span data-ttu-id="e80ff-129">За</span><span class="sxs-lookup"><span data-stu-id="e80ff-129">Daily</span></span>
- <span data-ttu-id="e80ff-130">Запуск</span><span class="sxs-lookup"><span data-stu-id="e80ff-130">Weekly</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e80ff-131">-RecurrenceValue</span><span class="sxs-lookup"><span data-stu-id="e80ff-131">-RecurrenceValue</span></span>
<span data-ttu-id="e80ff-132">Указывает периодичность создания резервной копии.</span><span class="sxs-lookup"><span data-stu-id="e80ff-132">Specifies how often to make a backup.</span></span>
<span data-ttu-id="e80ff-133">Этот параметр использует единицу, указанную в параметре *RecurrenceType* .</span><span class="sxs-lookup"><span data-stu-id="e80ff-133">This parameter uses the unit specified by the *RecurrenceType* parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e80ff-134">-RetentionCount</span><span class="sxs-lookup"><span data-stu-id="e80ff-134">-RetentionCount</span></span>
<span data-ttu-id="e80ff-135">Указывает количество дней, в течение которых будет храниться резервная копия.</span><span class="sxs-lookup"><span data-stu-id="e80ff-135">Specifies the number of days to keep a backup.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e80ff-136">-StartFromDateTime</span><span class="sxs-lookup"><span data-stu-id="e80ff-136">-StartFromDateTime</span></span>
<span data-ttu-id="e80ff-137">Указывает дату, с которой начинается создание резервных копий.</span><span class="sxs-lookup"><span data-stu-id="e80ff-137">Specifies the date from which to start making backups.</span></span>
<span data-ttu-id="e80ff-138">Значение по умолчанию — текущее время.</span><span class="sxs-lookup"><span data-stu-id="e80ff-138">The default value is the current time.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e80ff-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e80ff-139">CommonParameters</span></span>
<span data-ttu-id="e80ff-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e80ff-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e80ff-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e80ff-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e80ff-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e80ff-142">INPUTS</span></span>

### <span data-ttu-id="e80ff-143">Ничего</span><span class="sxs-lookup"><span data-stu-id="e80ff-143">None</span></span>

## <span data-ttu-id="e80ff-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e80ff-144">OUTPUTS</span></span>

### <span data-ttu-id="e80ff-145">BackupScheduleUpdateRequest</span><span class="sxs-lookup"><span data-stu-id="e80ff-145">BackupScheduleUpdateRequest</span></span>
<span data-ttu-id="e80ff-146">Этот командлет возвращает объект **BackupScheduleUpdateRequest** , содержащий сведения об обновленных расписаниях резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="e80ff-146">This cmdlet returns a **BackupScheduleUpdateRequest** object that contains information about updated backup schedules.</span></span>

## <span data-ttu-id="e80ff-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="e80ff-147">NOTES</span></span>

## <span data-ttu-id="e80ff-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e80ff-148">RELATED LINKS</span></span>

[<span data-ttu-id="e80ff-149">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span><span class="sxs-lookup"><span data-stu-id="e80ff-149">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span></span>](./New-AzureStorSimpleDeviceBackupScheduleAddConfig.md)

[<span data-ttu-id="e80ff-150">Set-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="e80ff-150">Set-AzureStorSimpleDeviceBackupPolicy</span></span>](./Set-AzureStorSimpleDeviceBackupPolicy.md)


