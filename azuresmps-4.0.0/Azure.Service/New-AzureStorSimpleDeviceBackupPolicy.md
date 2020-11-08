---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: EFAE7117-9B8B-4CB9-B4D9-3F08DCE1816E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 405b9d427c7e59dfb3628806a878d57a281a6b4e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076208"
---
# <span data-ttu-id="928b6-101">New-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="928b6-101">New-AzureStorSimpleDeviceBackupPolicy</span></span>

## <span data-ttu-id="928b6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="928b6-102">SYNOPSIS</span></span>
<span data-ttu-id="928b6-103">Создание политики резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="928b6-103">Creates a backup policy.</span></span>

## <span data-ttu-id="928b6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="928b6-104">SYNTAX</span></span>

```
New-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> -BackupPolicyName <String>
 -BackupSchedulesToAdd <PSObject[]> -VolumeIdsToAdd <PSObject[]> [-WaitForComplete] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="928b6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="928b6-105">DESCRIPTION</span></span>
<span data-ttu-id="928b6-106">Командлет **New-AzureStorSimpleDeviceBackupPolicy** создает политику резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="928b6-106">The **New-AzureStorSimpleDeviceBackupPolicy** cmdlet creates a backup policy.</span></span>
<span data-ttu-id="928b6-107">Политика резервного копирования состоит из одного или нескольких расписаний архивации, которые могут выполняться на одном или нескольких томах.</span><span class="sxs-lookup"><span data-stu-id="928b6-107">A backup policy contains one or more backup schedules that can run on one or more volumes.</span></span>
<span data-ttu-id="928b6-108">Чтобы создать расписание резервного копирования, используйте командлет **New-AzureStorSimpleDeviceBackupScheduleAddConfig** .</span><span class="sxs-lookup"><span data-stu-id="928b6-108">To create a backup schedule, use the **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet.</span></span>

## <span data-ttu-id="928b6-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="928b6-109">EXAMPLES</span></span>

### <span data-ttu-id="928b6-110">Пример 1: Создание политики архивации</span><span class="sxs-lookup"><span data-stu-id="928b6-110">Example 1: Create a backup policy</span></span>
```
PS C:\>$Schedule01 = New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType LocalSnapshot -RecurrenceType Daily -RecurrenceValue 10 -RetentionCount 5 -Enabled $True
PS C:\> $Schedule02 = New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType CloudSnapshot -RecurrenceType Hourly -RecurrenceValue 1 -RetentionCount 5 -Enabled $True
PS C:\> $ScheduleArray = @()
PS C:\> $ScheduleArray += $Schedule01
PS C:\> $ScheduleArray += $Schedule02
PS C:\> $DeviceContainer = Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm"
PS C:\> $Volume = $(Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeContainer $DeviceContainer[0])
PS C:\> $VolumeArray = @()
PS C:\> $VolumeArray += $Volume[0].InstanceId
PS C:\> New-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyName "GeneralPolicy07" -BackupSchedulesToAdd $ScheduleArray -VolumeIdsToAdd $VolumeArray
VERBOSE: ClientRequestId: e9d6771e-c323-47b9-b424-cb98f8ed0273_PS
VERBOSE: ClientRequestId: db0e7c86-d0d2-4a5a-b1cb-182494cba027_PS
VERBOSE: ClientRequestId: 77708dfd-a386-4999-b7ed-5d53e288ae83_PS


JobId        : d4ce5340-d5d1-4471-9cc8-013193f021b3
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your add operation has completed successfully. 
VERBOSE: ClientRequestId: bbf7e9b9-b493-40b3-8348-f15bcfc4da8a_PS
BackupSchedules          : {36d21096-bbd1-47b7-91b5-40ad1792d992, 505fc91f-deb5-4dca-bfcb-98c20b75ebcc}
Volumes                  : {volume03}
BackupPolicyCreationType : BySaaS
LastBackup               : 01-01-2010 05:30:00
NextBackup               : 16-12-2014 01:13:43
SchedulesCount           : 2
SSMHostName              : 
VolumesCount             : 1
InstanceId               : 8799c2f0-8850-4e91-aa23-ee18c67da8bd
Name                     : GeneralPolicy07
OperationInProgress      : None
```

<span data-ttu-id="928b6-111">Первая команда создает объект конфигурации расписания резервного копирования с помощью командлета **New-AzureStorSimpleDeviceBackupScheduleAddConfig** , а затем сохраняет этот объект в переменной $Schedule 01.</span><span class="sxs-lookup"><span data-stu-id="928b6-111">The first command creates a backup schedule configuration object by using the **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet, and then stores that object in the $Schedule01 variable.</span></span>

<span data-ttu-id="928b6-112">Вторая команда создает другой объект конфигурации резервного копирования с помощью **New-AzureStorSimpleDeviceBackupScheduleAddConfig** , а затем сохраняет этот объект в переменной $Schedule 02.</span><span class="sxs-lookup"><span data-stu-id="928b6-112">The second command creates another backup configuration object by using **New-AzureStorSimpleDeviceBackupScheduleAddConfig** , and then stores that object in the $Schedule02 variable.</span></span>

<span data-ttu-id="928b6-113">Третья команда создает пустую переменную массива с именем $ScheduleArray.</span><span class="sxs-lookup"><span data-stu-id="928b6-113">The third command creates an empty array variable, named $ScheduleArray.</span></span>
<span data-ttu-id="928b6-114">Следующие две команды добавляют объекты, созданные в первых двух командах, для $ScheduleArray.</span><span class="sxs-lookup"><span data-stu-id="928b6-114">The next two commands add the objects created in the first two commands to $ScheduleArray.</span></span>

<span data-ttu-id="928b6-115">Шестая команда получает контейнер тома для устройства с именем Contoso63-AppVm с помощью командлета **Get-AzureStorSimpleDeviceVolumeContainer** , а затем сохраняет этот объект-контейнер в переменной $DeviceContainer.</span><span class="sxs-lookup"><span data-stu-id="928b6-115">The sixth command gets a volume container for the device named Contoso63-AppVm by using the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet, and then stores that container object in the $DeviceContainer variable.</span></span>

<span data-ttu-id="928b6-116">Седьмая команда получает том для контейнера тома, хранящегося в первом члене $DeviceContainer с помощью командлета **Get-AzureStorSimpleDeviceVolume** , а затем сохраняет этот том в переменной $Volume.</span><span class="sxs-lookup"><span data-stu-id="928b6-116">The seventh command gets a volume for the volume container stored in the first member of $DeviceContainer by using the **Get-AzureStorSimpleDeviceVolume** cmdlet, and then stores that volume in the $Volume variable.</span></span>

<span data-ttu-id="928b6-117">Восьмая команда создает пустую переменную массива с именем $VolumeArray.</span><span class="sxs-lookup"><span data-stu-id="928b6-117">The eighth command creates an empty array variable, named $VolumeArray.</span></span>
<span data-ttu-id="928b6-118">Следующая команда добавляет идентификатор тома в $VolumeArray.</span><span class="sxs-lookup"><span data-stu-id="928b6-118">The next command adds a volume ID to $VolumeArray.</span></span>
<span data-ttu-id="928b6-119">Это значение определяет том, хранящийся в $Volume, на котором запускается политика резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="928b6-119">This value identifies the volume, stored in $Volume, on which the backup policy runs.</span></span>
<span data-ttu-id="928b6-120">Вы можете добавить дополнительные идентификаторы томов для $VolumeArray.</span><span class="sxs-lookup"><span data-stu-id="928b6-120">You can add additional volume IDs to $VolumeArray.</span></span>

<span data-ttu-id="928b6-121">Последняя команда создает политику резервного копирования с именем GeneralPolicy07 для устройства с именем Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="928b6-121">The final command creates the backup policy named GeneralPolicy07 for the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="928b6-122">Команда задает объекты конфигурации расписания, хранящиеся в $ScheduleArray.</span><span class="sxs-lookup"><span data-stu-id="928b6-122">The command specifies the schedule configuration objects stored in $ScheduleArray.</span></span>
<span data-ttu-id="928b6-123">Команда задает том или тома, к которым применяется политика в $VolumeArray.</span><span class="sxs-lookup"><span data-stu-id="928b6-123">The command specifies the volume or volumes to which to apply the policy in $VolumeArray.</span></span>
<span data-ttu-id="928b6-124">Политику резервного копирования можно проверить с помощью командлета **Get-AzureStorSimpleDeviceBackupPolicy** .</span><span class="sxs-lookup"><span data-stu-id="928b6-124">You can verify the backup policy by using the **Get-AzureStorSimpleDeviceBackupPolicy** cmdlet.</span></span>

## <span data-ttu-id="928b6-125">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="928b6-125">PARAMETERS</span></span>

### <span data-ttu-id="928b6-126">-BackupPolicyName</span><span class="sxs-lookup"><span data-stu-id="928b6-126">-BackupPolicyName</span></span>
<span data-ttu-id="928b6-127">Задает имя политики резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="928b6-127">Specifies the name of the backup policy.</span></span>

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

### <span data-ttu-id="928b6-128">-BackupSchedulesToAdd</span><span class="sxs-lookup"><span data-stu-id="928b6-128">-BackupSchedulesToAdd</span></span>
<span data-ttu-id="928b6-129">Задает массив объектов **BackupScheduleBase** , которые нужно добавить в политику.</span><span class="sxs-lookup"><span data-stu-id="928b6-129">Specifies an array of **BackupScheduleBase** objects to add to the policy.</span></span>
<span data-ttu-id="928b6-130">Каждый объект представляет расписание.</span><span class="sxs-lookup"><span data-stu-id="928b6-130">Each object represents a schedule.</span></span>
<span data-ttu-id="928b6-131">Политика резервного копирования состоит из одного или нескольких расписаний.</span><span class="sxs-lookup"><span data-stu-id="928b6-131">A backup policy contains one or more schedules.</span></span>
<span data-ttu-id="928b6-132">Чтобы получить объект **BackupScheduleBase** , используйте командлет **New-AzureStorSimpleDeviceBackupScheduleAddConfig** .</span><span class="sxs-lookup"><span data-stu-id="928b6-132">To obtain a **BackupScheduleBase** object, use the **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="928b6-133">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="928b6-133">-DeviceName</span></span>
<span data-ttu-id="928b6-134">Указывает имя устройства StorSimple, на котором нужно создать политику резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="928b6-134">Specifies the name of the StorSimple device on which to create the backup policy.</span></span>

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

### <span data-ttu-id="928b6-135">-Profile</span><span class="sxs-lookup"><span data-stu-id="928b6-135">-Profile</span></span>
<span data-ttu-id="928b6-136">Указывает профиль Azure.</span><span class="sxs-lookup"><span data-stu-id="928b6-136">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="928b6-137">-VolumeIdsToAdd</span><span class="sxs-lookup"><span data-stu-id="928b6-137">-VolumeIdsToAdd</span></span>
<span data-ttu-id="928b6-138">Задает массив идентификаторов томов, которые нужно добавить в политику резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="928b6-138">Specifies an array of the IDs of volumes to add to the backup policy.</span></span>

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="928b6-139">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="928b6-139">-WaitForComplete</span></span>
<span data-ttu-id="928b6-140">Указывает на то, что этот командлет ожидает завершения операции до того, как она возвратит управление на консоль Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="928b6-140">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="928b6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="928b6-141">CommonParameters</span></span>
<span data-ttu-id="928b6-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="928b6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="928b6-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="928b6-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="928b6-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="928b6-144">INPUTS</span></span>

### <span data-ttu-id="928b6-145">Ничего</span><span class="sxs-lookup"><span data-stu-id="928b6-145">None</span></span>

## <span data-ttu-id="928b6-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="928b6-146">OUTPUTS</span></span>

### <span data-ttu-id="928b6-147">BackupPolicy</span><span class="sxs-lookup"><span data-stu-id="928b6-147">BackupPolicy</span></span>
<span data-ttu-id="928b6-148">Этот командлет возвращает объект **BackupPolicy** , содержащий новые расписания и тома.</span><span class="sxs-lookup"><span data-stu-id="928b6-148">This cmdlet returns a **BackupPolicy** object that contains the new schedules and volumes.</span></span>

## <span data-ttu-id="928b6-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="928b6-149">NOTES</span></span>

## <span data-ttu-id="928b6-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="928b6-150">RELATED LINKS</span></span>

[<span data-ttu-id="928b6-151">Get-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="928b6-151">Get-AzureStorSimpleDeviceBackupPolicy</span></span>](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="928b6-152">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="928b6-152">Get-AzureStorSimpleDeviceVolume</span></span>](./Get-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="928b6-153">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="928b6-153">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="928b6-154">Remove-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="928b6-154">Remove-AzureStorSimpleDeviceBackupPolicy</span></span>](./Remove-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="928b6-155">Set-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="928b6-155">Set-AzureStorSimpleDeviceBackupPolicy</span></span>](./Set-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="928b6-156">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span><span class="sxs-lookup"><span data-stu-id="928b6-156">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span></span>](./New-AzureStorSimpleDeviceBackupScheduleAddConfig.md)


