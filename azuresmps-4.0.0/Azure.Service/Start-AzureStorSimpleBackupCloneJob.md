---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 403AD2BF-5D03-4B48-A635-E08216FFFC0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 07df96f59b2278d804312d1076965ffed43c2569
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075748"
---
# <span data-ttu-id="0d16f-101">Start-AzureStorSimpleBackupCloneJob</span><span class="sxs-lookup"><span data-stu-id="0d16f-101">Start-AzureStorSimpleBackupCloneJob</span></span>

## <span data-ttu-id="0d16f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0d16f-102">SYNOPSIS</span></span>
<span data-ttu-id="0d16f-103">Запускает задание, которое создает точную копию резервной копии на устройстве.</span><span class="sxs-lookup"><span data-stu-id="0d16f-103">Starts a job that clones a backup on a device.</span></span>

## <span data-ttu-id="0d16f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0d16f-104">SYNTAX</span></span>

### <span data-ttu-id="0d16f-105">Пустой (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0d16f-105">Empty (Default)</span></span>
```
Start-AzureStorSimpleBackupCloneJob -BackupId <String> -Snapshot <Snapshot> -CloneVolumeName <String>
 [-TargetAccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0d16f-106">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="0d16f-106">IdentifyByName</span></span>
```
Start-AzureStorSimpleBackupCloneJob -SourceDeviceName <String> -TargetDeviceName <String> -BackupId <String>
 -Snapshot <Snapshot> -CloneVolumeName <String>
 [-TargetAccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0d16f-107">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="0d16f-107">IdentifyById</span></span>
```
Start-AzureStorSimpleBackupCloneJob -SourceDeviceId <String> -TargetDeviceId <String> -BackupId <String>
 -Snapshot <Snapshot> -CloneVolumeName <String>
 [-TargetAccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0d16f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d16f-108">DESCRIPTION</span></span>
<span data-ttu-id="0d16f-109">Командлет **Start-AzureStorSimpleBackupCloneJob** запускает задание, которое копирует существующую резервную копию на устройстве StorSimple.</span><span class="sxs-lookup"><span data-stu-id="0d16f-109">The **Start-AzureStorSimpleBackupCloneJob** cmdlet starts a job that clones an existing backup on a StorSimple device.</span></span>

## <span data-ttu-id="0d16f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0d16f-110">EXAMPLES</span></span>

### <span data-ttu-id="0d16f-111">Пример 1: клонирование резервной копии на другой том с помощью имен устройств</span><span class="sxs-lookup"><span data-stu-id="0d16f-111">Example 1: Clone a backup to a different volume by using device names</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "ContosoDev07" -First 1
PS C:\> $Acrs = Get-AzureStorSimpleAccessControlRecord -ACRName "Acr01"
PS C:\> Start-AzureStorSimpleBackupCloneJob -SourceDeviceName "ContosoDev07 -TargetDeviceName "ContosoDev07" -BackupId $Backup.InstanceId -Snapshot $Backup.Snapshots[0] -CloneVolumeName "cloned_volume11" -TargetAccessControlRecords $Acrs
VERBOSE: ClientRequestId: 43d8b4dc-39da-4ec5-92f6-be1f499155e9_PS
VERBOSE: ClientRequestId: be7a73a7-980c-4ba2-82d4-f6a7ee0eac0a_PS
VERBOSE: ClientRequestId: ee02aaae-d366-43d2-a229-8761d6db39f1_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 9b81d9f9-3e31-49be-a8cd-1b1c6afdb744_PS
bd05baee-36d0-48f4-8b1e-8119c4133446
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId bd05baee-36d0-48f4-8b1e-8119c4133446 for tracking the job's status
```

<span data-ttu-id="0d16f-112">Первая команда получает первую резервную копию для устройства с именем ContosoDev07 с помощью командлета **Get-AzureStorSimpleDeviceBackup** .</span><span class="sxs-lookup"><span data-stu-id="0d16f-112">The first command gets the first backup for the device named ContosoDev07 by using the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>
<span data-ttu-id="0d16f-113">Команда хранит эти резервные копии в переменной $Backup.</span><span class="sxs-lookup"><span data-stu-id="0d16f-113">The command stores that backup in the $Backup variable.</span></span>

<span data-ttu-id="0d16f-114">Вторая команда получает доступ к записям управления доступом с помощью командлета **Get-AzureStorSimpleAccessControlRecord** .</span><span class="sxs-lookup"><span data-stu-id="0d16f-114">The second command gets access control records by using the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="0d16f-115">Команда сохраняет результат в переменной $Acrs.</span><span class="sxs-lookup"><span data-stu-id="0d16f-115">The command stores the result in the $Acrs variable.</span></span>

<span data-ttu-id="0d16f-116">Последняя команда запускает задание, которое копирует указанную резервную копию тома на устройство на другой том того же устройства.</span><span class="sxs-lookup"><span data-stu-id="0d16f-116">The final command begins a job that clones a specified backup of a volume on a device to a different volume on the same device.</span></span>
<span data-ttu-id="0d16f-117">В этом примере задается имя устройства.</span><span class="sxs-lookup"><span data-stu-id="0d16f-117">This example specifies the device by name.</span></span>
<span data-ttu-id="0d16f-118">В команде используются значения, хранящиеся в $Backup и $Acrs.</span><span class="sxs-lookup"><span data-stu-id="0d16f-118">The command uses the values stored in $Backup and $Acrs.</span></span>
<span data-ttu-id="0d16f-119">Команда возвращает идентификатор задания.</span><span class="sxs-lookup"><span data-stu-id="0d16f-119">The command returns the ID of the job.</span></span>

### <span data-ttu-id="0d16f-120">Пример 2: клонирование резервной копии на другой том с помощью идентификаторов устройств</span><span class="sxs-lookup"><span data-stu-id="0d16f-120">Example 2: Clone a backup to a different volume by using device IDs</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName ContosoDev07 -First 1
PS C:\> $Acrs = Get-AzureStorSimpleAccessControlRecord -ACRName "Acr01"
PS C:\> Start-AzureStorSimpleBackupCloneJob -SourceDeviceId "be7a73a7-980c-4ba2-82d4-f6a7ee0eacbb" -TargetDeviceId "be7a73a7-980c-4ba2-82d4-f6a7ee0eacbb" -BackupId $Backup.InstanceId -Snapshot $Backup.Snapshots[0] -CloneVolumeName "cloned_volume11" -TargetAccessControlRecords $Acrs
VERBOSE: ClientRequestId: 43d8b4dc-39da-4ec5-92f6-be1f499155e9_PS
VERBOSE: ClientRequestId: be7a73a7-980c-4ba2-82d4-f6a7ee0eac0a_PS
VERBOSE: ClientRequestId: ee02aaae-d366-43d2-a229-8761d6db39f1_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 9b81d9f9-3e31-49be-a8cd-1b1c6afdb744_PS
bd05baee-36d0-48f4-8b1e-8119c4133446
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId bd05baee-36d0-48f4-8b1e-8119c4133446 for tracking the job's status
```

<span data-ttu-id="0d16f-121">Первая команда получает первую резервную копию для устройства с именем ContosoDev07 с помощью командлета **Get-AzureStorSimpleDeviceBackup** .</span><span class="sxs-lookup"><span data-stu-id="0d16f-121">The first command gets the first backup for the device named ContosoDev07 by using the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>
<span data-ttu-id="0d16f-122">Команда хранит эти резервные копии в переменной $Backup.</span><span class="sxs-lookup"><span data-stu-id="0d16f-122">The command stores that backup in the $Backup variable.</span></span>

<span data-ttu-id="0d16f-123">Вторая команда получает доступ к записям управления доступом с помощью командлета **Get-AzureStorSimpleAccessControlRecord** .</span><span class="sxs-lookup"><span data-stu-id="0d16f-123">The second command gets access control records by using the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="0d16f-124">Команда сохраняет результат в переменной $Acrs.</span><span class="sxs-lookup"><span data-stu-id="0d16f-124">The command stores the result in the $Acrs variable.</span></span>

<span data-ttu-id="0d16f-125">Последняя команда запускает задание, которое копирует указанную резервную копию тома на устройство на другой том того же устройства.</span><span class="sxs-lookup"><span data-stu-id="0d16f-125">The final command begins a job that clones a specified backup of a volume on a device to a different volume on the same device.</span></span>
<span data-ttu-id="0d16f-126">В этом примере задается устройство по ИДЕНТИФИКАТОРу устройства.</span><span class="sxs-lookup"><span data-stu-id="0d16f-126">This example specifies the device by device ID.</span></span>
<span data-ttu-id="0d16f-127">В команде используются значения, хранящиеся в $Backup и $Acrs.</span><span class="sxs-lookup"><span data-stu-id="0d16f-127">The command uses the values stored in $Backup and $Acrs.</span></span>
<span data-ttu-id="0d16f-128">Команда возвращает идентификатор задания.</span><span class="sxs-lookup"><span data-stu-id="0d16f-128">The command returns the ID of the job.</span></span>

### <span data-ttu-id="0d16f-129">Пример 3: клонирование резервной копии на том, находящиеся на другом устройстве, с помощью имен устройств</span><span class="sxs-lookup"><span data-stu-id="0d16f-129">Example 3: Clone a backup to a volume on a different device by using device names</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "ContosoDev07" -First 1
PS C:\> $Acrs = Get-AzureStorSimpleAccessControlRecord -ACRName "Acr01"
PS C:\> Start-AzureStorSimpleBackupCloneJob -SourceDeviceName "ContosoDev07" -TargetDeviceName "ContosoDev12" -BackupId $Backup.InstanceId -Snapshot $Backup.Snapshots[0] -CloneVolumeName "cloned_volume11" -TargetAccessControlRecords $Acrs
VERBOSE: ClientRequestId: 43d8b4dc-39da-4ec5-92f6-be1f499155e9_PS
VERBOSE: ClientRequestId: be7a73a7-980c-4ba2-82d4-f6a7ee0eac0a_PS
VERBOSE: ClientRequestId: ee02aaae-d366-43d2-a229-8761d6db39f1_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 9b81d9f9-3e31-49be-a8cd-1b1c6afdb744_PS
bd05baee-36d0-48f4-8b1e-8119c4133446
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId bd05baee-36d0-48f4-8b1e-8119c4133446 for tracking the job's status
```

<span data-ttu-id="0d16f-130">Первая команда получает первую резервную копию для устройства с именем ContosoDev07 с помощью командлета **Get-AzureStorSimpleDeviceBackup** .</span><span class="sxs-lookup"><span data-stu-id="0d16f-130">The first command gets the first backup for the device named ContosoDev07 by using the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>
<span data-ttu-id="0d16f-131">Команда хранит эти резервные копии в переменной $Backup.</span><span class="sxs-lookup"><span data-stu-id="0d16f-131">The command stores that backup in the $Backup variable.</span></span>

<span data-ttu-id="0d16f-132">Вторая команда получает доступ к записям управления доступом с помощью командлета **Get-AzureStorSimpleAccessControlRecord** .</span><span class="sxs-lookup"><span data-stu-id="0d16f-132">The second command gets access control records by using the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="0d16f-133">Команда сохраняет результат в переменной $Acrs.</span><span class="sxs-lookup"><span data-stu-id="0d16f-133">The command stores the result in the $Acrs variable.</span></span>

<span data-ttu-id="0d16f-134">Последняя команда запускает задание, которое копирует указанную резервную копию тома на устройстве на том другого устройства.</span><span class="sxs-lookup"><span data-stu-id="0d16f-134">The final command begins a job that clones a specified backup of a volume on a device to a volume on a different device.</span></span>
<span data-ttu-id="0d16f-135">В этом примере задаются устройства по имени.</span><span class="sxs-lookup"><span data-stu-id="0d16f-135">This example specifies the devices by name.</span></span>
<span data-ttu-id="0d16f-136">В команде используются значения, хранящиеся в $Backup и $Acrs.</span><span class="sxs-lookup"><span data-stu-id="0d16f-136">The command uses the values stored in $Backup and $Acrs.</span></span>
<span data-ttu-id="0d16f-137">Команда возвращает идентификатор задания.</span><span class="sxs-lookup"><span data-stu-id="0d16f-137">The command returns the ID of the job.</span></span>

### <span data-ttu-id="0d16f-138">Пример 4: клонирование резервной копии на другой том с помощью имен устройств и оператора конвейера</span><span class="sxs-lookup"><span data-stu-id="0d16f-138">Example 4: Clone a backup to a different volume by using device names and the pipeline operator</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName ContosoDev1 -First 1
PS C:\> Get-AzureStorSimpleAccessControlRecord -ACRName acr1 | Start-AzureStorSimpleBackupCloneJob -SourceDeviceName ContosoDev1 -TargetDeviceName ContosoDev1 -BackupId $backup.InstanceId -Snapshot $backup.Snapshots[0] -CloneVolumeName "cloned_vol1" 
VERBOSE: ClientRequestId: 1183a29d-63a9-408a-9065-032c92d317ee_PS
VERBOSE: ClientRequestId: e195717c-5920-4133-bdf0-c1201ebabf6f_PS
VERBOSE: ClientRequestId: ac16644d-bfd8-4edf-b1ad-f5df4ceb4df7_PS
VERBOSE: ClientRequestId: dcdcab7f-2aaa-496d-8a18-2e7449a70227_PS
VERBOSE: ClientRequestId: 6f92e422-eda9-4087-aefb-2257a49f5beb_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 646b280c-b51c-4812-b5c5-b7ca215f1c90_PS
a747d2dc-2876-474e-aea6-6546b255427e
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId a747d2dc-2876-474e-aea6-6546b255427e for tracking the job's status
VERBOSE: Access Control Record with given name acr11 is found!
```

<span data-ttu-id="0d16f-139">Первая команда получает первую резервную копию для устройства с именем ContosoDev07 с помощью командлета **Get-AzureStorSimpleDeviceBackup** .</span><span class="sxs-lookup"><span data-stu-id="0d16f-139">The first command gets the first backup for the device named ContosoDev07 by using the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>
<span data-ttu-id="0d16f-140">Команда хранит эти резервные копии в переменной $Backup.</span><span class="sxs-lookup"><span data-stu-id="0d16f-140">The command stores that backup in the $Backup variable.</span></span>

<span data-ttu-id="0d16f-141">Вторая команда получает доступ к записям управления доступом с помощью командлета **Get-AzureStorSimpleAccessControlRecord** .</span><span class="sxs-lookup"><span data-stu-id="0d16f-141">The second command gets access control records by using the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="0d16f-142">Команда передает результаты в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="0d16f-142">The command passes its results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0d16f-143">Текущий командлет запускает задание, которое копирует указанное резервное копирование тома на устройстве на другой том на том же устройстве.</span><span class="sxs-lookup"><span data-stu-id="0d16f-143">The current cmdlet begins a job that clones a specified backup of a volume on a device, to a different volume on the same device.</span></span>
<span data-ttu-id="0d16f-144">В этом примере задается имя устройства.</span><span class="sxs-lookup"><span data-stu-id="0d16f-144">This example specifies the device by name.</span></span>
<span data-ttu-id="0d16f-145">В команде используется значение, хранящееся в $Backup.</span><span class="sxs-lookup"><span data-stu-id="0d16f-145">The command uses the value stored in $Backup.</span></span>
<span data-ttu-id="0d16f-146">Команда принимает значение параметра *TargetAccessControlRecords* из конвейера.</span><span class="sxs-lookup"><span data-stu-id="0d16f-146">The command takes the value of the *TargetAccessControlRecords* parameter from the pipeline.</span></span>
<span data-ttu-id="0d16f-147">Команда возвращает идентификатор задания.</span><span class="sxs-lookup"><span data-stu-id="0d16f-147">The command returns the ID of the job.</span></span>

## <span data-ttu-id="0d16f-148">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0d16f-148">PARAMETERS</span></span>

### <span data-ttu-id="0d16f-149">-BackupId</span><span class="sxs-lookup"><span data-stu-id="0d16f-149">-BackupId</span></span>
<span data-ttu-id="0d16f-150">Указывает ИД экземпляра резервной копии, которую нужно клонировать.</span><span class="sxs-lookup"><span data-stu-id="0d16f-150">Specifies the instance ID of the backup to clone.</span></span>

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

### <span data-ttu-id="0d16f-151">-CloneVolumeName</span><span class="sxs-lookup"><span data-stu-id="0d16f-151">-CloneVolumeName</span></span>
<span data-ttu-id="0d16f-152">Задает имя для нового клонированного тома на целевом устройстве.</span><span class="sxs-lookup"><span data-stu-id="0d16f-152">Specifies the name for the new cloned volume on the target device.</span></span>

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

### <span data-ttu-id="0d16f-153">-Force</span><span class="sxs-lookup"><span data-stu-id="0d16f-153">-Force</span></span>
<span data-ttu-id="0d16f-154">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="0d16f-154">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0d16f-155">-Profile</span><span class="sxs-lookup"><span data-stu-id="0d16f-155">-Profile</span></span>
<span data-ttu-id="0d16f-156">Указывает профиль Azure.</span><span class="sxs-lookup"><span data-stu-id="0d16f-156">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="0d16f-157">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="0d16f-157">-Snapshot</span></span>
<span data-ttu-id="0d16f-158">Указывает объект снимка, который копируется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="0d16f-158">Specifies the snapshot object that this cmdlet clones.</span></span>

```yaml
Type: Snapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d16f-159">-SourceDeviceId</span><span class="sxs-lookup"><span data-stu-id="0d16f-159">-SourceDeviceId</span></span>
<span data-ttu-id="0d16f-160">Указывает идентификатор экземпляра исходного устройства.</span><span class="sxs-lookup"><span data-stu-id="0d16f-160">Specifies the instance ID of the source device.</span></span>
<span data-ttu-id="0d16f-161">Этот командлет копирует обратно из исходного устройства.</span><span class="sxs-lookup"><span data-stu-id="0d16f-161">This cmdlet clones the back from the source device.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d16f-162">-SourceDeviceName</span><span class="sxs-lookup"><span data-stu-id="0d16f-162">-SourceDeviceName</span></span>
<span data-ttu-id="0d16f-163">Указывает имя исходного устройства.</span><span class="sxs-lookup"><span data-stu-id="0d16f-163">Specifies the name of the source device.</span></span>
<span data-ttu-id="0d16f-164">Этот командлет копирует обратно из исходного устройства.</span><span class="sxs-lookup"><span data-stu-id="0d16f-164">This cmdlet clones the back from the source device.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d16f-165">-TargetAccessControlRecords</span><span class="sxs-lookup"><span data-stu-id="0d16f-165">-TargetAccessControlRecords</span></span>
<span data-ttu-id="0d16f-166">Определяет записи управления доступом.</span><span class="sxs-lookup"><span data-stu-id="0d16f-166">Specifies the access control records.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d16f-167">-TargetDeviceId</span><span class="sxs-lookup"><span data-stu-id="0d16f-167">-TargetDeviceId</span></span>
<span data-ttu-id="0d16f-168">Указывает идентификатор экземпляра целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="0d16f-168">Specifies the instance ID of the target device.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d16f-169">-TargetDeviceName</span><span class="sxs-lookup"><span data-stu-id="0d16f-169">-TargetDeviceName</span></span>
<span data-ttu-id="0d16f-170">Указывает имя устройства, на которое этот командлет создает копию резервной копии.</span><span class="sxs-lookup"><span data-stu-id="0d16f-170">Specifies the name of the device to which this cmdlet clones the backup.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d16f-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d16f-171">CommonParameters</span></span>
<span data-ttu-id="0d16f-172">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0d16f-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d16f-173">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d16f-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d16f-174">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0d16f-174">INPUTS</span></span>

### <span data-ttu-id="0d16f-175">Снимок, список AccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="0d16f-175">Snapshot, List of AccessControlRecord</span></span>
<span data-ttu-id="0d16f-176">Вы можете передавать в этот командлет объекты **моментального снимка** или список объектов **AccessControlRecord** .</span><span class="sxs-lookup"><span data-stu-id="0d16f-176">You can pipe **Snapshot** objects or a list of **AccessControlRecord** objects to this cmdlet.</span></span>

## <span data-ttu-id="0d16f-177">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d16f-177">OUTPUTS</span></span>

## <span data-ttu-id="0d16f-178">Пуск</span><span class="sxs-lookup"><span data-stu-id="0d16f-178">NOTES</span></span>

## <span data-ttu-id="0d16f-179">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0d16f-179">RELATED LINKS</span></span>

[<span data-ttu-id="0d16f-180">Get-AzureStorSimpleDeviceBackup</span><span class="sxs-lookup"><span data-stu-id="0d16f-180">Get-AzureStorSimpleDeviceBackup</span></span>](./Get-AzureStorSimpleDeviceBackup.md)

[<span data-ttu-id="0d16f-181">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="0d16f-181">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)


