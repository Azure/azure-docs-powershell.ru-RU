---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: EE7EC812-640B-4672-B23C-673F912F0EDC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 945d06ddc1be6d2b0864b0421a5a087e14d98218
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075528"
---
# <span data-ttu-id="a89b6-101">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span><span class="sxs-lookup"><span data-stu-id="a89b6-101">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span></span>

## <span data-ttu-id="a89b6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a89b6-102">SYNOPSIS</span></span>
<span data-ttu-id="a89b6-103">Создает объект конфигурации расписания резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="a89b6-103">Creates a backup schedule configuration object.</span></span>

## <span data-ttu-id="a89b6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a89b6-104">SYNTAX</span></span>

```
New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType <String> -RecurrenceType <String>
 -RecurrenceValue <Int32> -RetentionCount <Int64> [-StartFromDateTime <String>] -Enabled <Boolean>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a89b6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a89b6-105">DESCRIPTION</span></span>
<span data-ttu-id="a89b6-106">Командлет **New-AzureStorSimpleDeviceBackupScheduleAddConfig** создает объект конфигурации **BackupScheduleBase** .</span><span class="sxs-lookup"><span data-stu-id="a89b6-106">The **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet creates a **BackupScheduleBase** configuration object.</span></span>
<span data-ttu-id="a89b6-107">Используйте этот объект конфигурации для создания новой политики резервного копирования с помощью командлета **New-AzureStorSimpleDeviceBackupPolicy** .</span><span class="sxs-lookup"><span data-stu-id="a89b6-107">Use this configuration object to create new backup policy by using the **New-AzureStorSimpleDeviceBackupPolicy** cmdlet.</span></span>

## <span data-ttu-id="a89b6-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a89b6-108">EXAMPLES</span></span>

### <span data-ttu-id="a89b6-109">Пример 1: создание резервного объекта конфигурации</span><span class="sxs-lookup"><span data-stu-id="a89b6-109">Example 1: Create a backup configuration object</span></span>
```
PS C:\>New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType CloudSnapshot -RecurrenceType Daily -RecurrenceValue 1 -RetentionCount 100 -Enabled $True
VERBOSE: ClientRequestId: 426a79ee-fed3-4d3d-9123-e371f83222b3_PS


BackupType     : CloudSnapshot
Recurrence     : Microsoft.WindowsAzure.Management.StorSimple.Models.ScheduleRecurrence
RetentionCount : 100
StartTime      : 2014-12-16T00:37:19+05:30
Status         : Enabled
```

<span data-ttu-id="a89b6-110">Эта команда создает базовый объект расписания резервного копирования для резервных копий облачных снимков.</span><span class="sxs-lookup"><span data-stu-id="a89b6-110">This command creates a backup schedule base object for cloud snapshot backups.</span></span>
<span data-ttu-id="a89b6-111">Резервное копирование выполняется каждый день, и резервные копии хранятся в течение 100 дней.</span><span class="sxs-lookup"><span data-stu-id="a89b6-111">The backup occurs every day, and the backups are kept for 100 days.</span></span>
<span data-ttu-id="a89b6-112">Это расписание включается по умолчанию, которое является текущим временем.</span><span class="sxs-lookup"><span data-stu-id="a89b6-112">This schedule is enabled from the default time, which is the current time.</span></span>

## <span data-ttu-id="a89b6-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a89b6-113">PARAMETERS</span></span>

### <span data-ttu-id="a89b6-114">-BackupType</span><span class="sxs-lookup"><span data-stu-id="a89b6-114">-BackupType</span></span>
<span data-ttu-id="a89b6-115">Указывает тип резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="a89b6-115">Specifies the backup type.</span></span>
<span data-ttu-id="a89b6-116">Допустимые значения: LocalSnapshot и CloudSnapshot.</span><span class="sxs-lookup"><span data-stu-id="a89b6-116">Valid values are: LocalSnapshot and CloudSnapshot.</span></span>

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

### <span data-ttu-id="a89b6-117">-Включено</span><span class="sxs-lookup"><span data-stu-id="a89b6-117">-Enabled</span></span>
<span data-ttu-id="a89b6-118">Указывает, следует ли включить расписание резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="a89b6-118">Indicates whether to enable the backup schedule.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a89b6-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="a89b6-119">-Profile</span></span>
<span data-ttu-id="a89b6-120">Указывает профиль Azure.</span><span class="sxs-lookup"><span data-stu-id="a89b6-120">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="a89b6-121">-RecurrenceType</span><span class="sxs-lookup"><span data-stu-id="a89b6-121">-RecurrenceType</span></span>
<span data-ttu-id="a89b6-122">Указывает тип повторения для этого расписания резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="a89b6-122">Specifies the type of recurrence for this backup schedule.</span></span>
<span data-ttu-id="a89b6-123">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="a89b6-123">Valid values are:</span></span> 

- <span data-ttu-id="a89b6-124">Течение</span><span class="sxs-lookup"><span data-stu-id="a89b6-124">Minutes</span></span>
- <span data-ttu-id="a89b6-125">Почасовой</span><span class="sxs-lookup"><span data-stu-id="a89b6-125">Hourly</span></span>
- <span data-ttu-id="a89b6-126">За</span><span class="sxs-lookup"><span data-stu-id="a89b6-126">Daily</span></span>
- <span data-ttu-id="a89b6-127">Запуск</span><span class="sxs-lookup"><span data-stu-id="a89b6-127">Weekly</span></span>

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

### <span data-ttu-id="a89b6-128">-RecurrenceValue</span><span class="sxs-lookup"><span data-stu-id="a89b6-128">-RecurrenceValue</span></span>
<span data-ttu-id="a89b6-129">Указывает периодичность создания резервной копии.</span><span class="sxs-lookup"><span data-stu-id="a89b6-129">Specifies how often to make a backup.</span></span>
<span data-ttu-id="a89b6-130">Этот параметр использует единицу, указанную в параметре *RecurrenceType* .</span><span class="sxs-lookup"><span data-stu-id="a89b6-130">This parameter uses the unit specified by the *RecurrenceType* parameter.</span></span>

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

### <span data-ttu-id="a89b6-131">-RetentionCount</span><span class="sxs-lookup"><span data-stu-id="a89b6-131">-RetentionCount</span></span>
<span data-ttu-id="a89b6-132">Указывает количество дней, в течение которых будет храниться резервная копия.</span><span class="sxs-lookup"><span data-stu-id="a89b6-132">Specifies the number of days to keep a backup.</span></span>

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

### <span data-ttu-id="a89b6-133">-StartFromDateTime</span><span class="sxs-lookup"><span data-stu-id="a89b6-133">-StartFromDateTime</span></span>
<span data-ttu-id="a89b6-134">Указывает дату, с которой начинается создание резервных копий.</span><span class="sxs-lookup"><span data-stu-id="a89b6-134">Specifies the date from which to start making backups.</span></span>
<span data-ttu-id="a89b6-135">Значение по умолчанию — текущее время.</span><span class="sxs-lookup"><span data-stu-id="a89b6-135">The default value is the current time.</span></span>

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

### <span data-ttu-id="a89b6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a89b6-136">CommonParameters</span></span>
<span data-ttu-id="a89b6-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a89b6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a89b6-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a89b6-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a89b6-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a89b6-139">INPUTS</span></span>

### <span data-ttu-id="a89b6-140">Ничего</span><span class="sxs-lookup"><span data-stu-id="a89b6-140">None</span></span>

## <span data-ttu-id="a89b6-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a89b6-141">OUTPUTS</span></span>

### <span data-ttu-id="a89b6-142">BackupScheduleBase</span><span class="sxs-lookup"><span data-stu-id="a89b6-142">BackupScheduleBase</span></span>
<span data-ttu-id="a89b6-143">Этот командлет возвращает объект **BackupScheduleBase** .</span><span class="sxs-lookup"><span data-stu-id="a89b6-143">This cmdlet returns a **BackupScheduleBase** object.</span></span>
<span data-ttu-id="a89b6-144">Используйте **BackupScheduleBase** для создания новой политики резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="a89b6-144">Use a **BackupScheduleBase** to construct new backup policy.</span></span>

## <span data-ttu-id="a89b6-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="a89b6-145">NOTES</span></span>

## <span data-ttu-id="a89b6-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a89b6-146">RELATED LINKS</span></span>

[<span data-ttu-id="a89b6-147">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="a89b6-147">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span></span>](./New-AzureStorSimpleDeviceBackupScheduleUpdateConfig.md)

[<span data-ttu-id="a89b6-148">New-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="a89b6-148">New-AzureStorSimpleDeviceBackupPolicy</span></span>](./New-AzureStorSimpleDeviceBackupPolicy.md)


