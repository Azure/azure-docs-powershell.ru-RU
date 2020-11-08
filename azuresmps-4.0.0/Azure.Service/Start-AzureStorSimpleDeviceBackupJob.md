---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 76826524-480F-458E-A996-A9DBACB8BA9E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4aa220334c75d3e6832698ec10fbad71896473d2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076027"
---
# <span data-ttu-id="e2608-101">Start-AzureStorSimpleDeviceBackupJob</span><span class="sxs-lookup"><span data-stu-id="e2608-101">Start-AzureStorSimpleDeviceBackupJob</span></span>

## <span data-ttu-id="e2608-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e2608-102">SYNOPSIS</span></span>
<span data-ttu-id="e2608-103">Запуск нового задания, которое создает резервную копию из существующей политики резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="e2608-103">Starts a new job that creates a backup from an existing backup policy.</span></span>

## <span data-ttu-id="e2608-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e2608-104">SYNTAX</span></span>

### <span data-ttu-id="e2608-105">Пустой (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e2608-105">Empty (Default)</span></span>
```
Start-AzureStorSimpleDeviceBackupJob -DeviceName <String> -BackupPolicyId <String> [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e2608-106">BackupTypeGiven</span><span class="sxs-lookup"><span data-stu-id="e2608-106">BackupTypeGiven</span></span>
```
Start-AzureStorSimpleDeviceBackupJob -DeviceName <String> -BackupPolicyId <String> -BackupType <String>
 [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e2608-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2608-107">DESCRIPTION</span></span>
<span data-ttu-id="e2608-108">Командлет **Start-AzureStorSimpleDeviceBackupJob** запускает новое задание, которое создает резервную копию на основе существующей политики архивации на устройстве StorSimple.</span><span class="sxs-lookup"><span data-stu-id="e2608-108">The **Start-AzureStorSimpleDeviceBackupJob** cmdlet starts a new job that creates a backup from an existing backup policy on a StorSimple device.</span></span>
<span data-ttu-id="e2608-109">По умолчанию этот командлет создает локальную резервную копию моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="e2608-109">By default, this cmdlet creates a local snapshot backup.</span></span>
<span data-ttu-id="e2608-110">Чтобы создать резервную копию в облаке, укажите для параметра *BackupType* значение CloudSnapshot.</span><span class="sxs-lookup"><span data-stu-id="e2608-110">To create a cloud backup, specify a value of CloudSnapshot for the *BackupType* parameter.</span></span>

## <span data-ttu-id="e2608-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e2608-111">EXAMPLES</span></span>

### <span data-ttu-id="e2608-112">Пример 1: Создание локального резервного копирования моментальных снимков</span><span class="sxs-lookup"><span data-stu-id="e2608-112">Example 1: Create a local snapshot backup</span></span>
```
PS C:\>Start-AzureStorSimpleDeviceBackupJob -DeviceName "Contoso63-AppVm" -BackupPolicyId "de088eac-b283-4d92-b501-a759845fdf3f"
JobId                                                                StatusCode RequestId
-----                                                                ---------- ---------
fb9acdca-ed6f-4b69-93f2-5c0bce0a1e08                                 Accepted   456cf6bafd427103b71c07145e26d35c

VERBOSE: Your backup operation has been submitted for processing. Use commandlet "Get-AzureStorSimpleJob -JobId
fb9acdca-ed6f-4b69-93f2-5c0bce0a1e08" to track status.
```

<span data-ttu-id="e2608-113">Эта команда создает локальную резервную копию моментального снимка для указанного идентификатора политики.</span><span class="sxs-lookup"><span data-stu-id="e2608-113">This command creates a local snapshot backup for the specified policy ID.</span></span>
<span data-ttu-id="e2608-114">Эта команда запускает задание, а затем возвращает объект **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="e2608-114">This command starts the job, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="e2608-115">Чтобы просмотреть состояние задания, используйте командлет **Get-AzureStorSimpleTask** .</span><span class="sxs-lookup"><span data-stu-id="e2608-115">To see the status of the job, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

### <span data-ttu-id="e2608-116">Пример 2: создание резервной копии облачных снимков и ожидание завершения</span><span class="sxs-lookup"><span data-stu-id="e2608-116">Example 2: Create a cloud snapshot backup and wait to finish</span></span>
```
PS C:\>Start-AzureStorSimpleDeviceBackupJob -DeviceName "Contoso63-AppVm" -BackupPolicyId "de088eac-b283-4d92-b501-a759845fdf3f" -BackupType CloudSnapshot -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : fb9acdca-ed6f-4b69-93f2-5c0bce0a1e08
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : f28ecf6cf75a7f128ca18e6ae14f9003
```

<span data-ttu-id="e2608-117">Эта команда создает резервную копию облачного снимка для указанного идентификатора политики.</span><span class="sxs-lookup"><span data-stu-id="e2608-117">This command creates a cloud snapshot backup for the specified policy ID.</span></span>
<span data-ttu-id="e2608-118">Эта команда задает параметр *WaitForComplete* , поэтому команда выполняет задачу и возвращает объект **TaskStatusInfo** для задания.</span><span class="sxs-lookup"><span data-stu-id="e2608-118">This command specifies the *WaitForComplete* parameter, so the command completes the task, and then returns a **TaskStatusInfo** object for the job.</span></span>

## <span data-ttu-id="e2608-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e2608-119">PARAMETERS</span></span>

### <span data-ttu-id="e2608-120">-BackupPolicyId</span><span class="sxs-lookup"><span data-stu-id="e2608-120">-BackupPolicyId</span></span>
<span data-ttu-id="e2608-121">Указывает идентификатор политики резервного копирования, которая будет использоваться для создания резервной копии.</span><span class="sxs-lookup"><span data-stu-id="e2608-121">Specifies the ID of the backup policy to use to create the backup.</span></span>

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

### <span data-ttu-id="e2608-122">-BackupType</span><span class="sxs-lookup"><span data-stu-id="e2608-122">-BackupType</span></span>
<span data-ttu-id="e2608-123">Указывает тип резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="e2608-123">Specifies the backup type.</span></span>
<span data-ttu-id="e2608-124">Допустимые значения: LocalSnapshot и CloudSnapshot.</span><span class="sxs-lookup"><span data-stu-id="e2608-124">Valid values are: LocalSnapshot and CloudSnapshot.</span></span>

```yaml
Type: String
Parameter Sets: BackupTypeGiven
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2608-125">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="e2608-125">-DeviceName</span></span>
<span data-ttu-id="e2608-126">Указывает имя устройства StorSimple, на котором нужно запустить задание резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="e2608-126">Specifies the name of the StorSimple device on which to start the backup job.</span></span>

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

### <span data-ttu-id="e2608-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="e2608-127">-Profile</span></span>
<span data-ttu-id="e2608-128">Указывает профиль Azure.</span><span class="sxs-lookup"><span data-stu-id="e2608-128">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="e2608-129">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="e2608-129">-WaitForComplete</span></span>
<span data-ttu-id="e2608-130">Указывает на то, что этот командлет ожидает завершения операции до того, как она возвратит управление на консоль Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e2608-130">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="e2608-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2608-131">CommonParameters</span></span>
<span data-ttu-id="e2608-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e2608-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2608-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2608-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2608-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e2608-134">INPUTS</span></span>

### <span data-ttu-id="e2608-135">Ничего</span><span class="sxs-lookup"><span data-stu-id="e2608-135">None</span></span>

## <span data-ttu-id="e2608-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2608-136">OUTPUTS</span></span>

### <span data-ttu-id="e2608-137">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="e2608-137">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="e2608-138">Этот командлет возвращает объект **TaskStatusInfo** , если указан параметр *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="e2608-138">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="e2608-139">Если этот параметр не указан, функция возвращает объект **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="e2608-139">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="e2608-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="e2608-140">NOTES</span></span>

## <span data-ttu-id="e2608-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e2608-141">RELATED LINKS</span></span>

[<span data-ttu-id="e2608-142">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="e2608-142">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)

[<span data-ttu-id="e2608-143">Start-AzureStorSimpleDeviceBackupRestoreJob</span><span class="sxs-lookup"><span data-stu-id="e2608-143">Start-AzureStorSimpleDeviceBackupRestoreJob</span></span>](./Start-AzureStorSimpleDeviceBackupRestoreJob.md)


