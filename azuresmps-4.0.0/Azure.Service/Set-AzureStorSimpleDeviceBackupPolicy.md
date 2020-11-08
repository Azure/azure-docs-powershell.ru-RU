---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F619B52A-6BFD-43E4-B313-F4C8D95EA966
online version: ''
schema: 2.0.0
ms.openlocfilehash: 570fdc21d650666e1cededbea597a5ef34023596
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075852"
---
# <span data-ttu-id="aaa8a-101">Set-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="aaa8a-101">Set-AzureStorSimpleDeviceBackupPolicy</span></span>

## <span data-ttu-id="aaa8a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aaa8a-102">SYNOPSIS</span></span>
<span data-ttu-id="aaa8a-103">Обновление существующей политики резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="aaa8a-103">Updates an existing backup policy.</span></span>

## <span data-ttu-id="aaa8a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aaa8a-104">SYNTAX</span></span>

```
Set-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> -BackupPolicyId <String> -BackupPolicyName <String>
 [-BackupSchedulesToAdd <PSObject[]>] [-BackupSchedulesToUpdate <PSObject[]>]
 [-BackupScheduleIdsToDelete <PSObject[]>] [-VolumeIdsToUpdate <PSObject[]>] [-WaitForComplete]
 [-NewName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="aaa8a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aaa8a-105">DESCRIPTION</span></span>
<span data-ttu-id="aaa8a-106">Командлет **Set-AzureStorSimpleDeviceBackupPolicy** обновляет существующую политику резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="aaa8a-106">The **Set-AzureStorSimpleDeviceBackupPolicy** cmdlet updates an existing backup policy.</span></span>
<span data-ttu-id="aaa8a-107">Вы можете переименовать политику, добавить, обновить или удалить расписания и обновить тома, связанные с политикой.</span><span class="sxs-lookup"><span data-stu-id="aaa8a-107">You can rename the policy, add, update or delete schedules, and update the volumes associated with the policy.</span></span>

## <span data-ttu-id="aaa8a-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aaa8a-108">EXAMPLES</span></span>

### <span data-ttu-id="aaa8a-109">Пример 1: изменение имени политики резервного копирования</span><span class="sxs-lookup"><span data-stu-id="aaa8a-109">Example 1: Change the name of a backup policy</span></span>
```
PS C:\>Set-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyId "e6d9f1b3-a250-4d57-966a-039c8eaef9e9" -BackupPolicyName "UpdatedGeneralPolicy07" -WaitForComplete
VERBOSE: ClientRequestId: f4465b46-26cc-40ff-88da-7a28df88c35c_PS
VERBOSE: ClientRequestId: 5e33a35c-e089-47c1-b760-474635b1ead8_PS
VERBOSE: About to run a task to update your backuppolicy! 
VERBOSE: ClientRequestId: e379ebdb-667f-45a9-aafa-a6cd61e5f6f6_PS


JobId        : 9d621bfd-3faa-4d1c-b28b-45c5f4a96975
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your update operation has completed successfully. 
VERBOSE: ClientRequestId: 4fe965ea-4e12-4869-9d67-e42a24b6c5d8_PS
BackupSchedules          : {58e9cd7c-4c6a-4e33-9109-5ec0b8fcb2cc, b10e1bf4-ef0a-4ad3-8fde-eecfc9971dd2}
Volumes                  : {testvolume03}
BackupPolicyCreationType : BySaaS
LastBackup               : 12/16/2014 2:13:28 PM
NextBackup               : 12/16/2014 3:13:43 PM
SchedulesCount           : 2
SSMHostName              : 
VolumesCount             : 1
InstanceId               : e6d9f1b3-a250-4d57-966a-039c8eaef9e9
Name                     : UpdatedGeneralPolicy07
OperationInProgress      : None
```

<span data-ttu-id="aaa8a-110">Эта команда изменяет имя политики резервного копирования с указанным ИДЕНТИФИКАТОРом на UpdatedGeneralPolicy07.</span><span class="sxs-lookup"><span data-stu-id="aaa8a-110">This command changes the name of the backup policy that has the specified ID to UpdatedGeneralPolicy07.</span></span>
<span data-ttu-id="aaa8a-111">Эта команда задает параметр *WaitForComplete* , поэтому команда завершает задачу и возвращает объект **TaskStatusInfo** для задачи.</span><span class="sxs-lookup"><span data-stu-id="aaa8a-111">This command specifies the *WaitForComplete* parameter, so the command completes the task, and then returns a **TaskStatusInfo** object for the task.</span></span>

### <span data-ttu-id="aaa8a-112">Пример 2: Обновление расписания для политики архивации</span><span class="sxs-lookup"><span data-stu-id="aaa8a-112">Example 2: Update the schedule for a backup policy</span></span>
```
PS C:\>$UpdateConfig = New-AzureStorSimpleDeviceBackupScheduleUpdateConfig -Id "3a6c6247-6b4d-42e2-aa87-16f4f21476ea" -BackupType CloudSnapshot -RecurrenceType Daily -RecurrenceValue 3 -RetentionCount 2 -Enabled $True
PS C:\> $UpdateArray = @()
PS C:\> $UpdateArray += $UpdateConfig
PS C:\> Set-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyId "712605f6-eb03-4db8-8f79-e0ce64b2cce1" -BackupSchedulesToUpdate $UpdateArray
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 7b265417-a5f1-45ad-8fbc-33bad4f63ec9
JobSteps   : {Microsoft.WindowsAzure.Management.StorSimple.Models.JobStep, 
             Microsoft.WindowsAzure.Management.StorSimple.Models.JobStep, 
             Microsoft.WindowsAzure.Management.StorSimple.Models.JobStep, 
             Microsoft.WindowsAzure.Management.StorSimple.Models.JobStep...} 
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : d2e10d44e699b371a84db44d19daf1c3
```

<span data-ttu-id="aaa8a-113">Первая команда создает объект конфигурации обновления с помощью командлета **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** , а затем сохраняет его в переменной $UpdateConfig.</span><span class="sxs-lookup"><span data-stu-id="aaa8a-113">The first command creates an update configuration object by using the **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** cmdlet, and then stores it in the $UpdateConfig variable.</span></span>

<span data-ttu-id="aaa8a-114">Вторая команда создает новую переменную массива с именем $UpdateArray.</span><span class="sxs-lookup"><span data-stu-id="aaa8a-114">The second command creates a new array variable, named $UpdateArray.</span></span>
<span data-ttu-id="aaa8a-115">Следующая команда добавляет обновление, которое хранится в $UpdateConfig, в этот массив.</span><span class="sxs-lookup"><span data-stu-id="aaa8a-115">The next command adds the update stored in $UpdateConfig to that array.</span></span>
<span data-ttu-id="aaa8a-116">Вы можете добавить в массив более одного обновления.</span><span class="sxs-lookup"><span data-stu-id="aaa8a-116">You can add more than one update to the array.</span></span>

<span data-ttu-id="aaa8a-117">Последняя команда обновляет политику резервного копирования с указанным ИДЕНТИФИКАТОРом на устройстве с именем Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="aaa8a-117">The final command updates the backup policy that has the specified ID on the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="aaa8a-118">Политика теперь имеет обновленное расписание, которое хранится в $UpdateArray.</span><span class="sxs-lookup"><span data-stu-id="aaa8a-118">The policy now has the updated schedule stored in $UpdateArray.</span></span>

## <span data-ttu-id="aaa8a-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aaa8a-119">PARAMETERS</span></span>

### <span data-ttu-id="aaa8a-120">-BackupPolicyId</span><span class="sxs-lookup"><span data-stu-id="aaa8a-120">-BackupPolicyId</span></span>
<span data-ttu-id="aaa8a-121">Задает ИД экземпляра объекта **BackupPolicy** , который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="aaa8a-121">Specifies the instance ID of the **BackupPolicy** object to update.</span></span>

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

### <span data-ttu-id="aaa8a-122">-BackupPolicyName</span><span class="sxs-lookup"><span data-stu-id="aaa8a-122">-BackupPolicyName</span></span>
<span data-ttu-id="aaa8a-123">Задает новое имя для политики резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="aaa8a-123">Specifies a new name for the backup policy.</span></span>

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

### <span data-ttu-id="aaa8a-124">-BackupScheduleIdsToDelete</span><span class="sxs-lookup"><span data-stu-id="aaa8a-124">-BackupScheduleIdsToDelete</span></span>
<span data-ttu-id="aaa8a-125">Задает массив идентификаторов экземпляров объектов **BackupSchedule** , которые нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="aaa8a-125">Specifies an array of instance IDs of **BackupSchedule** objects to delete.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaa8a-126">-BackupSchedulesToAdd</span><span class="sxs-lookup"><span data-stu-id="aaa8a-126">-BackupSchedulesToAdd</span></span>
<span data-ttu-id="aaa8a-127">Задает массив объектов **BackupScheduleBase** , которые нужно добавить в политику.</span><span class="sxs-lookup"><span data-stu-id="aaa8a-127">Specifies an array of **BackupScheduleBase** objects to add to the policy.</span></span>
<span data-ttu-id="aaa8a-128">Чтобы получить объект **BackupScheduleBase** , используйте командлет **New-AzureStorSimpleDeviceBackupScheduleAddConfig** .</span><span class="sxs-lookup"><span data-stu-id="aaa8a-128">To obtain a **BackupScheduleBase** object, use the **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaa8a-129">-BackupSchedulesToUpdate</span><span class="sxs-lookup"><span data-stu-id="aaa8a-129">-BackupSchedulesToUpdate</span></span>
<span data-ttu-id="aaa8a-130">Задает массив объектов **BackupScheduleUpdateRequest** , которые нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="aaa8a-130">Specifies an array of **BackupScheduleUpdateRequest** objects to update.</span></span>
<span data-ttu-id="aaa8a-131">Чтобы получить объект **BackupScheduleUpdateRequest** , используйте командлет **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** .</span><span class="sxs-lookup"><span data-stu-id="aaa8a-131">To obtain a **BackupScheduleUpdateRequest** object, use the **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** cmdlet.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaa8a-132">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="aaa8a-132">-DeviceName</span></span>
<span data-ttu-id="aaa8a-133">Указывает имя устройства StorSimple, для которого нужно обновить политику резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="aaa8a-133">Specifies the name of the StorSimple device for which to update the backup policy.</span></span>

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

### <span data-ttu-id="aaa8a-134">-NewName</span><span class="sxs-lookup"><span data-stu-id="aaa8a-134">-NewName</span></span>
<span data-ttu-id="aaa8a-135">Указывает имя устройства.</span><span class="sxs-lookup"><span data-stu-id="aaa8a-135">Specifies a name for the device.</span></span>

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

### <span data-ttu-id="aaa8a-136">-Profile</span><span class="sxs-lookup"><span data-stu-id="aaa8a-136">-Profile</span></span>
<span data-ttu-id="aaa8a-137">Указывает профиль Azure.</span><span class="sxs-lookup"><span data-stu-id="aaa8a-137">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="aaa8a-138">-VolumeIdsToUpdate</span><span class="sxs-lookup"><span data-stu-id="aaa8a-138">-VolumeIdsToUpdate</span></span>
<span data-ttu-id="aaa8a-139">Указывает массив идентификаторов томов, для которых нужно обновить политики резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="aaa8a-139">Specifies an array of IDs of volumes for which to update backup policies.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaa8a-140">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="aaa8a-140">-WaitForComplete</span></span>
<span data-ttu-id="aaa8a-141">Указывает на то, что этот командлет ожидает завершения операции до того, как она возвратит управление на консоль Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="aaa8a-141">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaa8a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaa8a-142">CommonParameters</span></span>
<span data-ttu-id="aaa8a-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aaa8a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaa8a-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aaa8a-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaa8a-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aaa8a-145">INPUTS</span></span>

### <span data-ttu-id="aaa8a-146">Ничего</span><span class="sxs-lookup"><span data-stu-id="aaa8a-146">None</span></span>

## <span data-ttu-id="aaa8a-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aaa8a-147">OUTPUTS</span></span>

### <span data-ttu-id="aaa8a-148">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="aaa8a-148">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="aaa8a-149">Этот командлет возвращает объект **TaskStatusInfo** , если указан параметр *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="aaa8a-149">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="aaa8a-150">Если этот параметр не указан, функция возвращает объект **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="aaa8a-150">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="aaa8a-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="aaa8a-151">NOTES</span></span>

## <span data-ttu-id="aaa8a-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aaa8a-152">RELATED LINKS</span></span>

[<span data-ttu-id="aaa8a-153">Get-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="aaa8a-153">Get-AzureStorSimpleDeviceBackupPolicy</span></span>](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="aaa8a-154">New-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="aaa8a-154">New-AzureStorSimpleDeviceBackupPolicy</span></span>](./New-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="aaa8a-155">Remove-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="aaa8a-155">Remove-AzureStorSimpleDeviceBackupPolicy</span></span>](./Remove-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="aaa8a-156">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="aaa8a-156">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span></span>](./New-AzureStorSimpleDeviceBackupScheduleUpdateConfig.md)


