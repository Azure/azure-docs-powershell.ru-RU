---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A40879D2-371B-4CF1-BF1F-9E5C896EB89C
online version: ''
schema: 2.0.0
ms.openlocfilehash: d5ffe0a6e5a2d6ae181f4396eae2b5732f527843
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076290"
---
# <span data-ttu-id="790e1-101">Get-AzureStorSimpleDeviceBackup</span><span class="sxs-lookup"><span data-stu-id="790e1-101">Get-AzureStorSimpleDeviceBackup</span></span>

## <span data-ttu-id="790e1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="790e1-102">SYNOPSIS</span></span>
<span data-ttu-id="790e1-103">Получает резервные копии с устройства.</span><span class="sxs-lookup"><span data-stu-id="790e1-103">Gets backups from a device.</span></span>

## <span data-ttu-id="790e1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="790e1-104">SYNTAX</span></span>

### <span data-ttu-id="790e1-105">Пустой (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="790e1-105">Empty (Default)</span></span>
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> [-From <String>] [-To <String>] [-First <Int32>]
 [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="790e1-106">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="790e1-106">IdentifyById</span></span>
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -BackupPolicyId <String> [-From <String>] [-To <String>]
 [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="790e1-107">IdentifyById2</span><span class="sxs-lookup"><span data-stu-id="790e1-107">IdentifyById2</span></span>
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -VolumeId <String> [-From <String>] [-To <String>]
 [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="790e1-108">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="790e1-108">IdentifyByObject</span></span>
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -BackupPolicy <BackupPolicyDetails> [-From <String>]
 [-To <String>] [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="790e1-109">IdentifyByObject2</span><span class="sxs-lookup"><span data-stu-id="790e1-109">IdentifyByObject2</span></span>
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -Volume <VirtualDisk> [-From <String>] [-To <String>]
 [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="790e1-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="790e1-110">DESCRIPTION</span></span>
<span data-ttu-id="790e1-111">Командлет **Get-AzureStorSimpleDeviceBackup** получает резервные копии с устройства.</span><span class="sxs-lookup"><span data-stu-id="790e1-111">The **Get-AzureStorSimpleDeviceBackup** cmdlet gets backups from a device.</span></span>
<span data-ttu-id="790e1-112">Вы можете указать политику архивации, том и время создания резервных копий.</span><span class="sxs-lookup"><span data-stu-id="790e1-112">You can specify the backup policy, volume, and creation time for backups.</span></span>

<span data-ttu-id="790e1-113">Этот командлет может возвращать максимум 100 резервных копий на первой странице.</span><span class="sxs-lookup"><span data-stu-id="790e1-113">This cmdlet can return a maximum of 100 backups in the first page.</span></span>
<span data-ttu-id="790e1-114">Если существует более 100 резервных копий, извлеките последующие страницы, используя *первый* и *пропущенный* параметры.</span><span class="sxs-lookup"><span data-stu-id="790e1-114">If more than 100 backups exist, retrieve subsequent pages by using the *First* and *Skip* parameters.</span></span>
<span data-ttu-id="790e1-115">Если задать значение 100 для параметра *пропустить* и 50 для *первого* , этот командлет не будет возвращать первые 100 результатов.</span><span class="sxs-lookup"><span data-stu-id="790e1-115">If you specify a value of 100 for *Skip* and 50 for *First* , this cmdlet does not return the first 100 results.</span></span>
<span data-ttu-id="790e1-116">Функция возвращает следующие 50 результаты после пропуска 100.</span><span class="sxs-lookup"><span data-stu-id="790e1-116">It returns the next 50 results after the 100 that it skips.</span></span>

## <span data-ttu-id="790e1-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="790e1-117">EXAMPLES</span></span>

### <span data-ttu-id="790e1-118">Пример 1: получение всех резервных копий на устройстве</span><span class="sxs-lookup"><span data-stu-id="790e1-118">Example 1: Get all backups on a device</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm"
InstanceId                           Name                               Type          BackupJobCreationType              CreatedOn                          SizeInBytes                       Snapshots                         SSMHostName                      
----------                           ----                               ----          ---------------------              ---------                          -----------                       ---------                         -----------                      
85074062-ef6a-408a-b6c9-2a0904bb99ca Snapshot_vg-all                    LocalSnapshot BySchedule                         4/15/2015 1:30:02 PM               9375913607168                     {Volume 1, Volume 4, Volume 3,                                     
                                                                                                                                                                                              Volume 2}                                                          
ebd87fa3-a9e2-49c9-a7e6-dada47071544 Cloud_Snapshot_vg-all              CloudSnapshot BySchedule                         4/15/2015 11:30:02 AM              9375913607168                     {Volume 1, Volume 4, Volume 3,                                     
                                                                                                                                                                                              Volume 2}                                                          
9f7a03be-8c39-474c-bf88-b2c7b54e833c Cloud_Snapshot_Vol3_clone VG       CloudSnapshot BySchedule                         4/15/2015 9:00:03 AM               1717986918400                     {Volume 3 Clone}                                                   
177b2dad-c0b2-42d6-b7bb-16926e54e9c6 VG Clones                          CloudSnapshot BySchedule                         4/15/2015 8:30:02 AM               5016521801728                     {Volume 1 Clone, Volume 3 Clone}                                   
49c470c0-eadb-40ac-9928-94018a8edcd4 Cloud_Snapshot_Vol1_clone VG       CloudSnapshot BySchedule                         4/15/2015 7:30:02 AM               3298534883328                     {Volume 1 Clone}                                                   
45dfd283-f924-4b45-93eb-b20650cadf43 vg-all                             LocalSnapshot Adhoc                              3/27/2015 9:12:15 PM               9375913607168                     {Volume 1, Volume 4, Volume 3,                                     
                                                                                                                                                                                              Volume 2}                                                          
2c3dd48d-824c-4298-82b5-fb44abb67a1e Test Group                         LocalSnapshot Adhoc                              3/27/2015 1:47:00 AM               5016521801728                     {Volume 1, Volume 3}
```

<span data-ttu-id="790e1-119">Эта команда получает все резервные копии, которые существуют на устройстве с именем Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="790e1-119">This command gets all backups that exist on the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="790e1-120">Если 100 количество резервных копий, разрешенное для первой страницы, превышает максимально допустимое, используйте параметры *First* и *Skip* для просмотра дополнительных результатов.</span><span class="sxs-lookup"><span data-stu-id="790e1-120">If there are more than the maximum of 100 backups allowed for the first page, use the *First* and *Skip* parameters to view additional results.</span></span>

### <span data-ttu-id="790e1-121">Пример 2: получение резервных копий, созданных между двумя датами</span><span class="sxs-lookup"><span data-stu-id="790e1-121">Example 2: Get backups created between two dates</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -From "9/7/2014" -To "10/7/2014" -First 2 -Skip 1
BackupJobCreationType : BySchedule
CreatedOn             : 10/5/2014 11:00:04 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : ec2fdf5c-c807-4f7b-a942-d4c4a9b68c44
Name                  : ContosoTSQA_Default
BackupJobCreationType : BySchedule
CreatedOn             : 10/4/2014 11:00:06 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : 5ac4f947-f4c6-4770-9000-2242e72fc6d3
Name                  : ContosoTSQA_DefaultVERBOSE: # of backups returned : 2
VERBOSE: More backups are available for your query. To access the next page of your result use \"-First 2 -Skip 3\" in
your commandlet
```

<span data-ttu-id="790e1-122">Эта команда получает резервные копии на устройстве с именем Contoso63-AppVm, созданных в 10/7/2014 и до 10/8/2014.</span><span class="sxs-lookup"><span data-stu-id="790e1-122">This command gets backups on the device named Contoso63-AppVm that were created on or after 10/7/2014 and on or before 10/8/2014.</span></span>
<span data-ttu-id="790e1-123">Этот командлет пропускает первый результат и возвращает первые два результата после этого первого результата.</span><span class="sxs-lookup"><span data-stu-id="790e1-123">This cmdlet skips the first result and returns the first two results after that first result.</span></span>
<span data-ttu-id="790e1-124">Измените значения для параметров *First* и *Skip* , чтобы просмотреть другие результаты.</span><span class="sxs-lookup"><span data-stu-id="790e1-124">Modify values for *First* and *Skip* to view other results.</span></span>

### <span data-ttu-id="790e1-125">Пример 3: получение резервных копий для идентификатора политики резервного копирования</span><span class="sxs-lookup"><span data-stu-id="790e1-125">Example 3: Get backups for a backup policy ID</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupPolicyId "de088eac-b283-4d92-b501-a759845fdf3f" -First 10 -From "9/7/2014"
BackupJobCreationType : BySchedule
CreatedOn             : 10/1/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : e1aec9f1-a321-443f-a058-ba78c749c2c2
Name                  : ContosoTSQA_Default
....... 

BackupJobCreationType : BySchedule
CreatedOn             : 9/29/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : f8041928-37b9-4048-a99c-2d3078943874
Name                  : ContosoTSQA_Default
VERBOSE: # of backups returned : 10
VERBOSE: More backups are available for your query. To access the next page of your result use \"-First 10 -Skip 10\"
in your commandlet
```

<span data-ttu-id="790e1-126">Эта команда получает резервные копии на устройстве с именем Contoso63-AppVm, созданной в указанную дату или ранее.</span><span class="sxs-lookup"><span data-stu-id="790e1-126">This command gets backups on the device named Contoso63-AppVm created on or before the specified date.</span></span>
<span data-ttu-id="790e1-127">Команда получает резервные копии, созданные с помощью политики резервного копирования с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="790e1-127">The command gets backups that were created by using the backup policy that has the specified ID.</span></span>
<span data-ttu-id="790e1-128">Эта команда задает *первый* параметр, поэтому он возвращает только первые 10 результатов.</span><span class="sxs-lookup"><span data-stu-id="790e1-128">This command specifies the *First* parameter, so it returns only the first 10 results.</span></span>

### <span data-ttu-id="790e1-129">Пример 4: получение резервных копий для объекта политики резервного копирования</span><span class="sxs-lookup"><span data-stu-id="790e1-129">Example 4: Get backups for a backup policy object</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyName "TSQATest_Default" | Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -First 10 -From "9/7/2014"
BackupJobCreationType : BySchedule
CreatedOn             : 10/1/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : e1aec9f1-a321-443f-a058-ba78c749c2c2
Name                  : ContosoTSQA_Default
....... 

BackupJobCreationType : BySchedule
CreatedOn             : 9/29/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : f8041928-37b9-4048-a99c-2d3078943874
Name                  : ContosoTSQA_Default
VERBOSE: # of backups returned : 10
VERBOSE: More backups are available for your query. To access the next page of your result use \"-First 10 -Skip 10\"
in your commandlet
```

<span data-ttu-id="790e1-130">Эта команда получает объект **BackupPolicyDetails** с помощью командлета **Get-AzureStorSimpleDeviceBackupPolicy** , а затем передает этот объект текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="790e1-130">This command gets a **BackupPolicyDetails** object by using the **Get-AzureStorSimpleDeviceBackupPolicy** cmdlet, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="790e1-131">Этот командлет получает резервные копии для устройства с именем Contoso63-AppVm, созданного с помощью политики резервного копирования из первой части команды.</span><span class="sxs-lookup"><span data-stu-id="790e1-131">That cmdlet gets backups for the device named Contoso63-AppVm created by using the backup policy from the first part of the command.</span></span>
<span data-ttu-id="790e1-132">Команда получает резервные копии, созданные до указанной даты или более ранней, так же, как и в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="790e1-132">The command gets backups created on or before the specified date, just as in the previous example.</span></span>
<span data-ttu-id="790e1-133">Эта команда возвращает только первые 10 результатов.</span><span class="sxs-lookup"><span data-stu-id="790e1-133">This command returns only the first 10 results.</span></span>

### <span data-ttu-id="790e1-134">Пример 5: получение резервной копии для идентификатора тома</span><span class="sxs-lookup"><span data-stu-id="790e1-134">Example 5: Get a backup for a volume ID</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -VolumeId "SS-VOL-246b9df1-11bb-4071-8043-f955cc406446" -First 1
BackupJobCreationType : BySchedule
CreatedOn             : 10/9/2014 11:00:10 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : 4fef4178-0145-404b-8257-7d958a380b8b
Name                  : ContosoTSQA_Default

VERBOSE: # of backups returned : 1
VERBOSE: No more backup sets are present for your query!
```

<span data-ttu-id="790e1-135">Эта команда получает резервную копию на устройстве, созданном на томе с указанным ИДЕНТИФИКАТОРом экземпляра.</span><span class="sxs-lookup"><span data-stu-id="790e1-135">This command gets a backup on the device that is created on the volume that has the specified instance ID.</span></span>
<span data-ttu-id="790e1-136">Эта команда задает *первый* параметр, поэтому она возвращает только первый из результатов.</span><span class="sxs-lookup"><span data-stu-id="790e1-136">This command specifies the *First* parameter, so it returns only the first one result.</span></span>

### <span data-ttu-id="790e1-137">Пример 6: получение резервной копии для имени тома</span><span class="sxs-lookup"><span data-stu-id="790e1-137">Example 6: Get a backup for a volume name</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "TSQATest03" | Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -First 1
BackupJobCreationType : BySchedule
CreatedOn             : 10/9/2014 11:00:10 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : 4fef4178-0145-404b-8257-7d958a380b8b
Name                  : ContosoTSQA_Default

VERBOSE: # of backups returned : 1
VERBOSE: No more backup sets are present for your query!
```

<span data-ttu-id="790e1-138">Эта команда получает объект **VirtualDisk** с помощью командлета **Get-AzureStorSimpleDeviceVolume** , а затем передает этот объект текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="790e1-138">This command gets a **VirtualDisk** object by using the **Get-AzureStorSimpleDeviceVolume** cmdlet, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="790e1-139">Этот командлет получает резервные копии для устройства с именем Contoso63-AppVm, созданного на томе из первой части команды.</span><span class="sxs-lookup"><span data-stu-id="790e1-139">That cmdlet gets backups for the device named Contoso63-AppVm created on the volume from the first part of the command.</span></span>
<span data-ttu-id="790e1-140">Эта команда возвращает только первый результат.</span><span class="sxs-lookup"><span data-stu-id="790e1-140">This command returns only the first result.</span></span>

## <span data-ttu-id="790e1-141">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="790e1-141">PARAMETERS</span></span>

### <span data-ttu-id="790e1-142">-BackupPolicy</span><span class="sxs-lookup"><span data-stu-id="790e1-142">-BackupPolicy</span></span>
<span data-ttu-id="790e1-143">Указывает объект **BackupPolicyDetails** .</span><span class="sxs-lookup"><span data-stu-id="790e1-143">Specifies a **BackupPolicyDetails** object.</span></span>
<span data-ttu-id="790e1-144">Этот командлет использует **InstanceId** этого объекта, чтобы определить, какие резервные копии нужно получить.</span><span class="sxs-lookup"><span data-stu-id="790e1-144">This cmdlet uses the **InstanceId** of this object to determine which backups to get.</span></span>
<span data-ttu-id="790e1-145">Чтобы получить объект **BackupPolicyDetails** , используйте командлет **Get-AzureStorSimpleDeviceBackupPolicy** .</span><span class="sxs-lookup"><span data-stu-id="790e1-145">To obtain a **BackupPolicyDetails** object, use the **Get-AzureStorSimpleDeviceBackupPolicy** cmdlet.</span></span>

```yaml
Type: BackupPolicyDetails
Parameter Sets: IdentifyByObject
Aliases: BackupPolicyDetails

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="790e1-146">-BackupPolicyId</span><span class="sxs-lookup"><span data-stu-id="790e1-146">-BackupPolicyId</span></span>
<span data-ttu-id="790e1-147">Задает идентификатор экземпляра политики резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="790e1-147">Specifies an instance ID of a backup policy.</span></span>
<span data-ttu-id="790e1-148">Этот командлет получает резервные копии устройств для политики, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="790e1-148">This cmdlet gets device backups for policy that this parameter specifies.</span></span>

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

### <span data-ttu-id="790e1-149">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="790e1-149">-DeviceName</span></span>
<span data-ttu-id="790e1-150">Указывает имя устройства StorSimple, для которого требуется получить резервные копии.</span><span class="sxs-lookup"><span data-stu-id="790e1-150">Specifies the name of the StorSimple device for which to get backups.</span></span>

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

### <span data-ttu-id="790e1-151">-First</span><span class="sxs-lookup"><span data-stu-id="790e1-151">-First</span></span>
<span data-ttu-id="790e1-152">Возвращает только указанное количество объектов.</span><span class="sxs-lookup"><span data-stu-id="790e1-152">Gets only the specified number of objects.</span></span>
<span data-ttu-id="790e1-153">Введите количество получаемых объектов.</span><span class="sxs-lookup"><span data-stu-id="790e1-153">Enter the number of objects to get.</span></span>

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

### <span data-ttu-id="790e1-154">-From</span><span class="sxs-lookup"><span data-stu-id="790e1-154">-From</span></span>
<span data-ttu-id="790e1-155">Указывает дату и время начала для резервных копий, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="790e1-155">Specifies the start date and time for the backups that this cmdlet gets.</span></span>

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

### <span data-ttu-id="790e1-156">-Profile</span><span class="sxs-lookup"><span data-stu-id="790e1-156">-Profile</span></span>
<span data-ttu-id="790e1-157">Указывает профиль Azure.</span><span class="sxs-lookup"><span data-stu-id="790e1-157">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="790e1-158">-Skip</span><span class="sxs-lookup"><span data-stu-id="790e1-158">-Skip</span></span>
<span data-ttu-id="790e1-159">Пропускает указанное количество объектов и возвращает оставшиеся объекты.</span><span class="sxs-lookup"><span data-stu-id="790e1-159">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="790e1-160">Введите количество объектов для пропуска.</span><span class="sxs-lookup"><span data-stu-id="790e1-160">Enter the number of objects to skip.</span></span>

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

### <span data-ttu-id="790e1-161">-To</span><span class="sxs-lookup"><span data-stu-id="790e1-161">-To</span></span>
<span data-ttu-id="790e1-162">Задает конечную дату и время для резервных копий, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="790e1-162">Specifies the end date and time for the backups that this cmdlet gets.</span></span>

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

### <span data-ttu-id="790e1-163">-Volume</span><span class="sxs-lookup"><span data-stu-id="790e1-163">-Volume</span></span>
<span data-ttu-id="790e1-164">Указывает объект **VirtualDisk** .</span><span class="sxs-lookup"><span data-stu-id="790e1-164">Specifies a **VirtualDisk** object.</span></span>
<span data-ttu-id="790e1-165">Этот командлет использует **InstanceId** этого объекта, чтобы определить том, на котором находятся резервные копии.</span><span class="sxs-lookup"><span data-stu-id="790e1-165">This cmdlet uses the **InstanceId** of this object to determine the volume in which backups exist.</span></span>
<span data-ttu-id="790e1-166">Чтобы получить объект **VirtualDisk** , используйте параметр **Get-AzureStorSimpleDeviceVolume** .</span><span class="sxs-lookup"><span data-stu-id="790e1-166">To obtain a **VirtualDisk** object, use the **Get-AzureStorSimpleDeviceVolume** parameter.</span></span>

```yaml
Type: VirtualDisk
Parameter Sets: IdentifyByObject2
Aliases: VirtualDiskInfo

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="790e1-167">-VolumeId</span><span class="sxs-lookup"><span data-stu-id="790e1-167">-VolumeId</span></span>
<span data-ttu-id="790e1-168">Указывает ИД экземпляра тома, на котором существуют резервные копии.</span><span class="sxs-lookup"><span data-stu-id="790e1-168">Specifies the instance ID of the volume in which backups exist.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById2
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="790e1-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="790e1-169">CommonParameters</span></span>
<span data-ttu-id="790e1-170">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="790e1-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="790e1-171">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="790e1-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="790e1-172">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="790e1-172">INPUTS</span></span>

### <span data-ttu-id="790e1-173">BackupPolicyDetails, VirtualDisk</span><span class="sxs-lookup"><span data-stu-id="790e1-173">BackupPolicyDetails, VirtualDisk</span></span>
<span data-ttu-id="790e1-174">Этот командлет принимает объекты **BackupPolicyDetails** и **VirtualDisk** .</span><span class="sxs-lookup"><span data-stu-id="790e1-174">This cmdlet accepts **BackupPolicyDetails** and **VirtualDisk** objects.</span></span>

## <span data-ttu-id="790e1-175">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="790e1-175">OUTPUTS</span></span>

### <span data-ttu-id="790e1-176">Оставлял\<Backup\></span><span class="sxs-lookup"><span data-stu-id="790e1-176">IList\<Backup\></span></span>
<span data-ttu-id="790e1-177">Этот командлет возвращает список объектов **резервного копирования** .</span><span class="sxs-lookup"><span data-stu-id="790e1-177">This cmdlet returns a list of **Backup** objects.</span></span>

## <span data-ttu-id="790e1-178">Пуск</span><span class="sxs-lookup"><span data-stu-id="790e1-178">NOTES</span></span>

## <span data-ttu-id="790e1-179">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="790e1-179">RELATED LINKS</span></span>

[<span data-ttu-id="790e1-180">Remove-AzureStorSimpleDeviceBackup</span><span class="sxs-lookup"><span data-stu-id="790e1-180">Remove-AzureStorSimpleDeviceBackup</span></span>](./Remove-AzureStorSimpleDeviceBackup.md)

[<span data-ttu-id="790e1-181">Get-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="790e1-181">Get-AzureStorSimpleDeviceBackupPolicy</span></span>](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="790e1-182">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="790e1-182">Get-AzureStorSimpleDeviceVolume</span></span>](./Get-AzureStorSimpleDeviceVolume.md)


