---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F9C8D0AA-ED97-43E8-ADB1-5AE1A4517666
online version: ''
schema: 2.0.0
ms.openlocfilehash: c524bb90d84df6ad3e37b552b957dac2d75b6a6c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075747"
---
# <span data-ttu-id="5622d-101">Start-AzureStorSimpleDeviceBackupRestoreJob</span><span class="sxs-lookup"><span data-stu-id="5622d-101">Start-AzureStorSimpleDeviceBackupRestoreJob</span></span>

## <span data-ttu-id="5622d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5622d-102">SYNOPSIS</span></span>
<span data-ttu-id="5622d-103">Запуск задания для восстановления резервной копии на устройстве StorSimple.</span><span class="sxs-lookup"><span data-stu-id="5622d-103">Starts a job that restores a backup on a StorSimple device.</span></span>

## <span data-ttu-id="5622d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5622d-104">SYNTAX</span></span>

### <span data-ttu-id="5622d-105">Пустой (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5622d-105">Empty (Default)</span></span>
```
Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName <String> -BackupId <String> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5622d-106">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="5622d-106">IdentifyById</span></span>
```
Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName <String> -BackupId <String> -SnapshotId <String>
 [-WaitForComplete] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5622d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5622d-107">DESCRIPTION</span></span>
<span data-ttu-id="5622d-108">Командлет **Start-AzureStorSimpleDeviceBackupRestoreJob** запускает задание, которое восстанавливает резервную копию на устройстве StorSimple.</span><span class="sxs-lookup"><span data-stu-id="5622d-108">The **Start-AzureStorSimpleDeviceBackupRestoreJob** cmdlet starts a job that restores a backup on a StorSimple device.</span></span>
<span data-ttu-id="5622d-109">Укажите идентификатор резервной копии и идентификатор необязательного снимка.</span><span class="sxs-lookup"><span data-stu-id="5622d-109">Specify a backup ID and an optional snapshot ID.</span></span>

## <span data-ttu-id="5622d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5622d-110">EXAMPLES</span></span>

### <span data-ttu-id="5622d-111">Пример 1: запуск задания для восстановления резервной копии</span><span class="sxs-lookup"><span data-stu-id="5622d-111">Example 1: Start a job to restore a backup</span></span>
```
PS C:\>Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName "Contoso63-AppVm" -BackupId "b3b50534-763c-4b05-9724-5ecf62bde721" -WaitForComplete
Confirm
Are you sure you want to restore the backup with backupId b3b50534-763c-4b05-9724-5ecf62bde721? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y


Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 217d0647-c001-4f43-9833-f8155a458e95
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : e0aa2dcd2f197a8588c40a067fe0e519
```

<span data-ttu-id="5622d-112">Эта команда запускает задание, которое восстанавливает объект резервного копирования с указанным ИДЕНТИФИКАТОРом и связанные с ним снимки на устройстве с именем Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="5622d-112">This command starts a job that restores the backup object that has the specified ID, and its associated snapshots, on the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="5622d-113">В команде указан параметр *WaitForComplete* , поэтому задание завершается до того, как командлет возвратит элемент управления на консоль.</span><span class="sxs-lookup"><span data-stu-id="5622d-113">The command specifies the *WaitForComplete* parameter, so the job finishes before the cmdlet returns control to the console.</span></span>

### <span data-ttu-id="5622d-114">Пример 2: запуск задания для восстановления определенного моментального снимка</span><span class="sxs-lookup"><span data-stu-id="5622d-114">Example 2: Start a job to restore a specific snapshot</span></span>
```
PS C:\>Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName "Contoso63-AppVm" -BackupId "b3b50534-763c-4b05-9724-5ecf62bde721" -SnapshotId "2d0cfad7-46bf-4266-8859-96549646e947_0000000000000000" -Force

The start job is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId 9102ed9a-078f-4648-a
721-3cffbba31336 for tracking the job status
```

<span data-ttu-id="5622d-115">Эта команда запускает задание, которое восстанавливает резервный снимок с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="5622d-115">This command starts a job that restores the backup snapshot that has the specified ID.</span></span>
<span data-ttu-id="5622d-116">Команда задает объект резервного копирования по ИДЕНТИФИКАТОРу на устройстве с именем Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="5622d-116">The command specifies the backup object by ID on the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="5622d-117">Команда задает параметр *Force* , поэтому она запускает задание без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="5622d-117">The command specifies the *Force* parameter, so it starts the job without prompting you to confirm.</span></span>

## <span data-ttu-id="5622d-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5622d-118">PARAMETERS</span></span>

### <span data-ttu-id="5622d-119">-BackupId</span><span class="sxs-lookup"><span data-stu-id="5622d-119">-BackupId</span></span>
<span data-ttu-id="5622d-120">Задает ИД экземпляра резервной копии для восстановления.</span><span class="sxs-lookup"><span data-stu-id="5622d-120">Specifies the instance ID of the backup to restore.</span></span>

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

### <span data-ttu-id="5622d-121">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="5622d-121">-DeviceName</span></span>
<span data-ttu-id="5622d-122">Указывает имя устройства StorSimple, на котором существует резервная копия.</span><span class="sxs-lookup"><span data-stu-id="5622d-122">Specifies the name of the StorSimple device on which the backup exists.</span></span>

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

### <span data-ttu-id="5622d-123">-Force</span><span class="sxs-lookup"><span data-stu-id="5622d-123">-Force</span></span>
<span data-ttu-id="5622d-124">Указывает на то, что этот командлет не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="5622d-124">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="5622d-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="5622d-125">-Profile</span></span>
<span data-ttu-id="5622d-126">Указывает профиль Azure.</span><span class="sxs-lookup"><span data-stu-id="5622d-126">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="5622d-127">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="5622d-127">-SnapshotId</span></span>
<span data-ttu-id="5622d-128">Указывает ИД экземпляра восстанавливаемого снимка.</span><span class="sxs-lookup"><span data-stu-id="5622d-128">Specifies the instance ID of the snapshot to restore.</span></span>

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

### <span data-ttu-id="5622d-129">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="5622d-129">-WaitForComplete</span></span>
<span data-ttu-id="5622d-130">Указывает на то, что этот командлет ожидает завершения операции до того, как она возвратит управление на консоль Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5622d-130">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="5622d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5622d-131">CommonParameters</span></span>
<span data-ttu-id="5622d-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5622d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5622d-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5622d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5622d-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5622d-134">INPUTS</span></span>

### <span data-ttu-id="5622d-135">Ничего</span><span class="sxs-lookup"><span data-stu-id="5622d-135">None</span></span>

## <span data-ttu-id="5622d-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5622d-136">OUTPUTS</span></span>

### <span data-ttu-id="5622d-137">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="5622d-137">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="5622d-138">Этот командлет возвращает объект **TaskStatusInfo** , если указан параметр *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="5622d-138">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="5622d-139">Если этот параметр не указан, функция возвращает объект **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="5622d-139">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="5622d-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="5622d-140">NOTES</span></span>

## <span data-ttu-id="5622d-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5622d-141">RELATED LINKS</span></span>

[<span data-ttu-id="5622d-142">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="5622d-142">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)

[<span data-ttu-id="5622d-143">Start-AzureStorSimpleDeviceBackupJob</span><span class="sxs-lookup"><span data-stu-id="5622d-143">Start-AzureStorSimpleDeviceBackupJob</span></span>](./Start-AzureStorSimpleDeviceBackupJob.md)


