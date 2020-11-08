---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 2001E040-5551-40C3-81D2-9A8334DE02BF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7692d4407df8fb4af8647ee0b4490abe73b2c937
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075558"
---
# <span data-ttu-id="69732-101">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="69732-101">Get-AzureStorSimpleJob</span></span>

## <span data-ttu-id="69732-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="69732-102">SYNOPSIS</span></span>
<span data-ttu-id="69732-103">Получает задания StorSimple.</span><span class="sxs-lookup"><span data-stu-id="69732-103">Gets StorSimple jobs.</span></span>

## <span data-ttu-id="69732-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="69732-104">SYNTAX</span></span>

```
Get-AzureStorSimpleJob [-DeviceName <String>] [-InstanceId <String>] [-Status <String>] [-Type <String>]
 [-From <DateTime>] [-To <DateTime>] [-Skip <Int32>] [-First <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="69732-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="69732-105">DESCRIPTION</span></span>
<span data-ttu-id="69732-106">Командлет **Get-AzureStorSimpleJob** получает задачи Azure StorSimple.</span><span class="sxs-lookup"><span data-stu-id="69732-106">The **Get-AzureStorSimpleJob** cmdlet gets Azure StorSimple jobs.</span></span>
<span data-ttu-id="69732-107">Укажите идентификатор экземпляра, чтобы получить конкретное задание.</span><span class="sxs-lookup"><span data-stu-id="69732-107">Specify an instance ID to get a specific job.</span></span>
<span data-ttu-id="69732-108">Укажите другие параметры, чтобы ограничить задания, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="69732-108">Specify other parameters to limit the jobs that this cmdlet gets.</span></span>

<span data-ttu-id="69732-109">Этот командлет возвращает не более 200 заданий.</span><span class="sxs-lookup"><span data-stu-id="69732-109">This cmdlet returns a maximum of 200 jobs.</span></span>
<span data-ttu-id="69732-110">Если существует более 200 заданий, получите оставшиеся задания с помощью параметров *First* и *Skip* .</span><span class="sxs-lookup"><span data-stu-id="69732-110">If more than 200 jobs exist, get the remaining jobs by using the *First* and *Skip* parameters.</span></span>
<span data-ttu-id="69732-111">Если задать значение 100 для параметра *пропустить* и 50 для *первого* , этот командлет не будет возвращать первые 100 результатов.</span><span class="sxs-lookup"><span data-stu-id="69732-111">If you specify a value of 100 for *Skip* and 50 for *First* , this cmdlet does not return the first 100 results.</span></span>
<span data-ttu-id="69732-112">Функция возвращает следующие 50 результаты после пропуска 100.</span><span class="sxs-lookup"><span data-stu-id="69732-112">It returns the next 50 results after the 100 that it skips.</span></span>

## <span data-ttu-id="69732-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="69732-113">EXAMPLES</span></span>

### <span data-ttu-id="69732-114">Пример 1: получение задания с помощью идентификатора</span><span class="sxs-lookup"><span data-stu-id="69732-114">Example 1: Get a job by using an ID</span></span>
```
PS C:\>Get-AzureStorSimpleJob -InstanceId "574f47e0-44e9-495c-b8a5-0203c57ebf6d"
BackupPolicy             : 
BackupTimeStamp          : 1/1/0001 12:00:00 AM
BackupType               : CloudSnapshot
DataStats                : Microsoft.WindowsAzure.Management.StorSimple.Models.DataStatistics
Device                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
Entity                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
ErrorDetails             : {}
HideProgressDetails      : False
InstanceId               : 574f47e0-44e9-495c-b8a5-0203c57ebf6d
IsInstantRestoreComplete : False
IsJobCancellable         : True
JobDetails               : Microsoft.WindowsAzure.Management.StorSimple.Models.JobStatusInfo
Name                     : 26447caf-59bb-41c9-a028-3224d296c7dc
Progress                 : 100
SourceDevice             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
SourceEntity             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
SourceVolume             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
Status                   : Completed
TimeStats                : Microsoft.WindowsAzure.Management.StorSimple.Models.TimeStatistics
Type                     : Backup
Volume                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
```

<span data-ttu-id="69732-115">Эта команда получает сведения о задании с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="69732-115">This command gets information for the job that has the specified ID.</span></span>

### <span data-ttu-id="69732-116">Пример 2: получение заданий с помощью имени устройства</span><span class="sxs-lookup"><span data-stu-id="69732-116">Example 2: Get jobs by using a device name</span></span>
```
PS C:\>Get-AzureStorSimpleJob -DeviceName "8600-Bravo 001" -First 2
InstanceId                           Type                         Status                                          DeviceName                                      StartTime                                       Progress                                       
----------                           ----                         ------                                          ----------                                      ---------                                       --------                                       
1997c33f-bfcc-4d08-9aba-28068340a1f9 Backup                       Running                                         8600-Bravo 001                                  4/15/2015 1:30:02 PM                            92                                             
85074062-ef6a-408a-b6c9-2a0904bb99ca Backup                       Completed                                       8600-Bravo 001                                  4/15/2015 1:30:02 PM                            100
```

<span data-ttu-id="69732-117">Эта команда получает сведения о заданиях для устройства с названием 8600-Bravo 001.</span><span class="sxs-lookup"><span data-stu-id="69732-117">This command gets information for the jobs for the device named 8600-Bravo 001.</span></span>
<span data-ttu-id="69732-118">Команда получает первые два задания для устройства.</span><span class="sxs-lookup"><span data-stu-id="69732-118">The command gets the first two jobs for the device.</span></span>

### <span data-ttu-id="69732-119">Пример 3: Получение завершенных заданий</span><span class="sxs-lookup"><span data-stu-id="69732-119">Example 3: Get completed jobs</span></span>
```
PS C:\>Get-AzureStorSimpleJob -Status "Completed" -Skip 10 -First 2
```

<span data-ttu-id="69732-120">Эта команда получает выполненные задания.</span><span class="sxs-lookup"><span data-stu-id="69732-120">This command gets completed jobs.</span></span>
<span data-ttu-id="69732-121">Команда возвращает только первые два задания после пропуска первых десяти заданий.</span><span class="sxs-lookup"><span data-stu-id="69732-121">The command gets only the first two jobs after it skips the first ten jobs.</span></span>

### <span data-ttu-id="69732-122">Пример 4: задания резервного копирования вручную</span><span class="sxs-lookup"><span data-stu-id="69732-122">Example 4: Get manual backup jobs</span></span>
```
PS C:\>Get-AzureStorSimpleJob -Type "ManualBackup"
```

<span data-ttu-id="69732-123">Эта команда получает задания типа резервного копирования вручную.</span><span class="sxs-lookup"><span data-stu-id="69732-123">This command gets jobs of the manual backup type.</span></span>

### <span data-ttu-id="69732-124">Пример 5: получение заданий между определенным временем</span><span class="sxs-lookup"><span data-stu-id="69732-124">Example 5: Get jobs between specified times</span></span>
```
PS C:\>$StartTime = Get-Date -Year 2015 -Month 3 -Day 10
PS C:\> $EndTime = Get-Date -Year 2015 -Month 3 -Day 11 -Hour 12 -Minute 15
PS C:\>Get-AzureStorSimpleJob -DeviceName "Device07" -From $StartTime -To $EndTime
```

<span data-ttu-id="69732-125">Первые две команды создают объекты **DateTime** с помощью командлета Get-Date.</span><span class="sxs-lookup"><span data-stu-id="69732-125">The first two commands create **DateTime** objects by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="69732-126">Команды хранят новые значения времен в переменных $StartTime и $EndTime.</span><span class="sxs-lookup"><span data-stu-id="69732-126">The commands store the new times in the $StartTime and $EndTime variables.</span></span>
<span data-ttu-id="69732-127">Для получения дополнительных сведений введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="69732-127">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="69732-128">Последняя команда получает задания для устройства с именем Device07 между временем, хранящимся в $StartTime и $EndTime.</span><span class="sxs-lookup"><span data-stu-id="69732-128">The final command gets jobs for the device named Device07 between the times stored in $StartTime and $EndTime.</span></span>

## <span data-ttu-id="69732-129">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="69732-129">PARAMETERS</span></span>

### <span data-ttu-id="69732-130">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="69732-130">-DeviceName</span></span>
<span data-ttu-id="69732-131">Указывает имя устройства StorSimple.</span><span class="sxs-lookup"><span data-stu-id="69732-131">Specifies the name of a StorSimple device.</span></span>

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

### <span data-ttu-id="69732-132">-First</span><span class="sxs-lookup"><span data-stu-id="69732-132">-First</span></span>
<span data-ttu-id="69732-133">Возвращает только указанное количество объектов.</span><span class="sxs-lookup"><span data-stu-id="69732-133">Gets only the specified number of objects.</span></span>
<span data-ttu-id="69732-134">Введите количество получаемых объектов.</span><span class="sxs-lookup"><span data-stu-id="69732-134">Enter the number of objects to get.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69732-135">-From</span><span class="sxs-lookup"><span data-stu-id="69732-135">-From</span></span>
<span data-ttu-id="69732-136">Указывает дату и время начала выполнения заданий, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="69732-136">Specifies the start date and time for the jobs that this cmdlet gets.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69732-137">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="69732-137">-InstanceId</span></span>
<span data-ttu-id="69732-138">Указывает ИД задания, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="69732-138">Specifies the ID of the job to get.</span></span>

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

### <span data-ttu-id="69732-139">-Profile</span><span class="sxs-lookup"><span data-stu-id="69732-139">-Profile</span></span>
<span data-ttu-id="69732-140">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="69732-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="69732-141">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="69732-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="69732-142">-Skip</span><span class="sxs-lookup"><span data-stu-id="69732-142">-Skip</span></span>
<span data-ttu-id="69732-143">Пропускает указанное количество объектов и возвращает оставшиеся объекты.</span><span class="sxs-lookup"><span data-stu-id="69732-143">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="69732-144">Введите количество объектов для пропуска.</span><span class="sxs-lookup"><span data-stu-id="69732-144">Enter the number of objects to skip.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69732-145">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="69732-145">-Status</span></span>
<span data-ttu-id="69732-146">Указывает состояние.</span><span class="sxs-lookup"><span data-stu-id="69732-146">Specifies the status.</span></span>
<span data-ttu-id="69732-147">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="69732-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="69732-148">Использующ</span><span class="sxs-lookup"><span data-stu-id="69732-148">Running</span></span>
- <span data-ttu-id="69732-149">Completed</span><span class="sxs-lookup"><span data-stu-id="69732-149">Completed</span></span>
- <span data-ttu-id="69732-150">Отменен</span><span class="sxs-lookup"><span data-stu-id="69732-150">Cancelled</span></span>
- <span data-ttu-id="69732-151">Ошибкой</span><span class="sxs-lookup"><span data-stu-id="69732-151">Failed</span></span>
- <span data-ttu-id="69732-152">Отмены</span><span class="sxs-lookup"><span data-stu-id="69732-152">Canceling</span></span>
- <span data-ttu-id="69732-153">CompletedWithErrors</span><span class="sxs-lookup"><span data-stu-id="69732-153">CompletedWithErrors</span></span>

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

### <span data-ttu-id="69732-154">-To</span><span class="sxs-lookup"><span data-stu-id="69732-154">-To</span></span>
<span data-ttu-id="69732-155">Задает конечную дату и время для задания, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="69732-155">Specifies the end date and time for the jobs that this cmdlet gets.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69732-156">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="69732-156">-Type</span></span>
<span data-ttu-id="69732-157">Указывает тип задания.</span><span class="sxs-lookup"><span data-stu-id="69732-157">Specifies the job type.</span></span>
<span data-ttu-id="69732-158">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="69732-158">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="69732-159">Копирование</span><span class="sxs-lookup"><span data-stu-id="69732-159">Backup</span></span>
- <span data-ttu-id="69732-160">ManualBackup</span><span class="sxs-lookup"><span data-stu-id="69732-160">ManualBackup</span></span>
- <span data-ttu-id="69732-161">Восстановление</span><span class="sxs-lookup"><span data-stu-id="69732-161">Restore</span></span>
- <span data-ttu-id="69732-162">CloneWorkflow</span><span class="sxs-lookup"><span data-stu-id="69732-162">CloneWorkflow</span></span>
- <span data-ttu-id="69732-163">DeviceRestore</span><span class="sxs-lookup"><span data-stu-id="69732-163">DeviceRestore</span></span>
- <span data-ttu-id="69732-164">Обновление</span><span class="sxs-lookup"><span data-stu-id="69732-164">Update</span></span>
- <span data-ttu-id="69732-165">SupportPackage</span><span class="sxs-lookup"><span data-stu-id="69732-165">SupportPackage</span></span>
- <span data-ttu-id="69732-166">VirtualApplianceProvisioning</span><span class="sxs-lookup"><span data-stu-id="69732-166">VirtualApplianceProvisioning</span></span>

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

### <span data-ttu-id="69732-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69732-167">CommonParameters</span></span>
<span data-ttu-id="69732-168">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="69732-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69732-169">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69732-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69732-170">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="69732-170">INPUTS</span></span>

### <span data-ttu-id="69732-171">Ничего</span><span class="sxs-lookup"><span data-stu-id="69732-171">None</span></span>
<span data-ttu-id="69732-172">Вы не можете передавать входные данные в этот командлет.</span><span class="sxs-lookup"><span data-stu-id="69732-172">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="69732-173">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="69732-173">OUTPUTS</span></span>

### <span data-ttu-id="69732-174">IList \<DeviceJobDetails\> , DeviceJobDetails</span><span class="sxs-lookup"><span data-stu-id="69732-174">IList\<DeviceJobDetails\>, DeviceJobDetails</span></span>
<span data-ttu-id="69732-175">Этот командлет возвращает список объектов сведений о задании или, если указан параметр *InstanceId* , возвращает один объект детализации задания.</span><span class="sxs-lookup"><span data-stu-id="69732-175">This cmdlet returns a list of job details objects, or, if you specify the *InstanceID* parameter, it returns a single job detail object.</span></span>

## <span data-ttu-id="69732-176">Пуск</span><span class="sxs-lookup"><span data-stu-id="69732-176">NOTES</span></span>

## <span data-ttu-id="69732-177">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="69732-177">RELATED LINKS</span></span>

[<span data-ttu-id="69732-178">Остановить-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="69732-178">Stop-AzureStorSimpleJob</span></span>](./Stop-AzureStorSimpleJob.md)


