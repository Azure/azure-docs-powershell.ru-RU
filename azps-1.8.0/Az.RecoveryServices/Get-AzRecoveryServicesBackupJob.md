---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 5dab5eaca48152dc573caf75f5d80737802bfcdf
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399827"
---
# <span data-ttu-id="7f9a3-101">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="7f9a3-101">Get-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="7f9a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f9a3-102">SYNOPSIS</span></span>
<span data-ttu-id="7f9a3-103">Возвращает задания резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="7f9a3-103">Gets Backup jobs.</span></span>

## <span data-ttu-id="7f9a3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7f9a3-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f9a3-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f9a3-105">DESCRIPTION</span></span>
<span data-ttu-id="7f9a3-106">Чтобы **получить задания резервного** копирования для определенного хранилища, можно получить задания резервного копирования Azure.</span><span class="sxs-lookup"><span data-stu-id="7f9a3-106">The **Get-AzRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>
<span data-ttu-id="7f9a3-107">Прежде чем использовать текущий Set-AzRecoveryServicesVaultContext, задате контекст хранилища с помощью Set-AzRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="7f9a3-107">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="7f9a3-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7f9a3-108">EXAMPLES</span></span>

### <span data-ttu-id="7f9a3-109">Пример 1. Все задания выполнения</span><span class="sxs-lookup"><span data-stu-id="7f9a3-109">Example 1: Get all in-progress jobs</span></span>
```
PS C:\>$Joblist = Get-AzRecoveryservicesBackupJob -Status Inprogress
PS C:\> $Joblist[0]
WorkloadName     Operation            Status               StartTime                 EndTime                                             
------------     ---------            ------               ---------                 -------                                             
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="7f9a3-110">Первая команда получает состояние выполнения задания как массива, а затем сохраняет его в $Joblist переменной.</span><span class="sxs-lookup"><span data-stu-id="7f9a3-110">The first command gets status of an in-progress job as an array, and then stores it in the $Joblist variable.</span></span>
<span data-ttu-id="7f9a3-111">Вторая команда отображает первый элемент в $Joblist массиве.</span><span class="sxs-lookup"><span data-stu-id="7f9a3-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="7f9a3-112">Пример 2. Получить все сбойные задания за последние 7 дней</span><span class="sxs-lookup"><span data-stu-id="7f9a3-112">Example 2: Get all failed jobs in the last 7 days</span></span>
```
PS C:\>Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed
```

<span data-ttu-id="7f9a3-113">Эта команда получает сбой заданий за последнюю неделю в хранилище.</span><span class="sxs-lookup"><span data-stu-id="7f9a3-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="7f9a3-114">Параметр *From* указывает время, прошедшее семь дней, указанное в UTC.</span><span class="sxs-lookup"><span data-stu-id="7f9a3-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="7f9a3-115">Команда не указывает значение параметра *To.*</span><span class="sxs-lookup"><span data-stu-id="7f9a3-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="7f9a3-116">Поэтому в нем используется значение по умолчанию для текущего времени.</span><span class="sxs-lookup"><span data-stu-id="7f9a3-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="7f9a3-117">Пример 3. Получить задание и дождаться завершения</span><span class="sxs-lookup"><span data-stu-id="7f9a3-117">Example 3: Get an in-progress job and wait for completion</span></span>
```
PS C:\> 
$Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress
$Job = $Jobs[0]
    while ( $Job.Status -ne Completed )
    {
       Write-Host "Waiting for completion..."
       Start-Sleep -Seconds 10
       $job = Get-AzBackAzureRmRecoveryServicesBackupJob  -Job $Job
    }
    Write-Host "Done!"
    Waiting for completion... 
    Waiting for completion... 
    Waiting for completion... 
    Done!
```

<span data-ttu-id="7f9a3-118">Этот сценарий оповестит первое задание, которое в настоящее время находится в процессе выполнения, пока задание не будет завершено.</span><span class="sxs-lookup"><span data-stu-id="7f9a3-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="7f9a3-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f9a3-119">PARAMETERS</span></span>

### <span data-ttu-id="7f9a3-120">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="7f9a3-120">-BackupManagementType</span></span>
<span data-ttu-id="7f9a3-121">Определяет тип управления резервной копией.</span><span class="sxs-lookup"><span data-stu-id="7f9a3-121">Specifies the Backup management type.</span></span>
<span data-ttu-id="7f9a3-122">В настоящее время поддерживается только AzureVM, AzureStorage.</span><span class="sxs-lookup"><span data-stu-id="7f9a3-122">Currently, only AzureVM, AzureStorage is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f9a3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f9a3-123">-DefaultProfile</span></span>
<span data-ttu-id="7f9a3-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7f9a3-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f9a3-125">-From</span><span class="sxs-lookup"><span data-stu-id="7f9a3-125">-From</span></span>
<span data-ttu-id="7f9a3-126">Начало в качестве объекта **даты и времени** для диапазона времени для заданий, которые получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f9a3-126">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="7f9a3-127">Чтобы получить объект **даты и времени,** используйте Get-Date даты.</span><span class="sxs-lookup"><span data-stu-id="7f9a3-127">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="7f9a3-128">Чтобы получить дополнительные сведения об **объектах даты и времени,** введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="7f9a3-128">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="7f9a3-129">Для дат используйте формат UTC.</span><span class="sxs-lookup"><span data-stu-id="7f9a3-129">Use UTC format for dates.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f9a3-130">-Job</span><span class="sxs-lookup"><span data-stu-id="7f9a3-130">-Job</span></span>
<span data-ttu-id="7f9a3-131">Имя задания резервного копирования, которое нужно получить.</span><span class="sxs-lookup"><span data-stu-id="7f9a3-131">Specifies the name of the Backup job to get.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f9a3-132">-JobId</span><span class="sxs-lookup"><span data-stu-id="7f9a3-132">-JobId</span></span>
<span data-ttu-id="7f9a3-133">Определяет код задания, которое получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f9a3-133">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="7f9a3-134">ID — это свойство InstanceId объекта **AzureRmRecoveryServicesBackupJob.**</span><span class="sxs-lookup"><span data-stu-id="7f9a3-134">The ID is the InstanceId property of an **AzureRmRecoveryServicesBackupJob** object.</span></span>
<span data-ttu-id="7f9a3-135">Чтобы получить объект **AzureRmRecoveryServicesBackupJob,** воспользуйтесь get-AzRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="7f9a3-135">To obtain an **AzureRmRecoveryServicesBackupJob** object, use Get-AzRecoveryServicesBackupJob.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f9a3-136">-Operation</span><span class="sxs-lookup"><span data-stu-id="7f9a3-136">-Operation</span></span>
<span data-ttu-id="7f9a3-137">Указывает операцию заданий, которые получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f9a3-137">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="7f9a3-138">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="7f9a3-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7f9a3-139">Резервное копирование</span><span class="sxs-lookup"><span data-stu-id="7f9a3-139">Backup</span></span>
- <span data-ttu-id="7f9a3-140">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="7f9a3-140">ConfigureBackup</span></span>
- <span data-ttu-id="7f9a3-141">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="7f9a3-141">DeleteBackupData</span></span>
- <span data-ttu-id="7f9a3-142">Регистрация</span><span class="sxs-lookup"><span data-stu-id="7f9a3-142">Register</span></span>
- <span data-ttu-id="7f9a3-143">"Восстановить"</span><span class="sxs-lookup"><span data-stu-id="7f9a3-143">Restore</span></span>
- <span data-ttu-id="7f9a3-144">"Отопретить"</span><span class="sxs-lookup"><span data-stu-id="7f9a3-144">UnProtect</span></span>
- <span data-ttu-id="7f9a3-145">Отоимкать регистрацию</span><span class="sxs-lookup"><span data-stu-id="7f9a3-145">Unregister</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobOperation]
Parameter Sets: (All)
Aliases:
Accepted values: Backup, Restore, ConfigureBackup, DisableBackup, DeleteBackupData

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f9a3-146">-Status</span><span class="sxs-lookup"><span data-stu-id="7f9a3-146">-Status</span></span>
<span data-ttu-id="7f9a3-147">Указывает состояние заданий, которые получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f9a3-147">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="7f9a3-148">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="7f9a3-148">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7f9a3-149">InProgress</span><span class="sxs-lookup"><span data-stu-id="7f9a3-149">InProgress</span></span>
- <span data-ttu-id="7f9a3-150">Сбой</span><span class="sxs-lookup"><span data-stu-id="7f9a3-150">Failed</span></span>
- <span data-ttu-id="7f9a3-151">Отменено</span><span class="sxs-lookup"><span data-stu-id="7f9a3-151">Cancelled</span></span>
- <span data-ttu-id="7f9a3-152">Отмена</span><span class="sxs-lookup"><span data-stu-id="7f9a3-152">Cancelling</span></span>
- <span data-ttu-id="7f9a3-153">Завершено</span><span class="sxs-lookup"><span data-stu-id="7f9a3-153">Completed</span></span>
- <span data-ttu-id="7f9a3-154">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="7f9a3-154">CompletedWithWarnings</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobStatus]
Parameter Sets: (All)
Aliases:
Accepted values: InProgress, Cancelling, Cancelled, Completed, CompletedWithWarnings, Failed

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f9a3-155">-To</span><span class="sxs-lookup"><span data-stu-id="7f9a3-155">-To</span></span>
<span data-ttu-id="7f9a3-156">Окончание в качестве объекта **даты и времени** для диапазона времени для заданий, которые получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f9a3-156">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="7f9a3-157">Значением по умолчанию является текущее системное время.</span><span class="sxs-lookup"><span data-stu-id="7f9a3-157">The default value is the current system time.</span></span>
<span data-ttu-id="7f9a3-158">Если этот параметр указан, необходимо также указать параметр *From.*</span><span class="sxs-lookup"><span data-stu-id="7f9a3-158">If you specify this parameter, you must also specify the *From* parameter.</span></span>
<span data-ttu-id="7f9a3-159">Для дат используйте формат UTC.</span><span class="sxs-lookup"><span data-stu-id="7f9a3-159">Use UTC format for dates.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f9a3-160">-VaultId</span><span class="sxs-lookup"><span data-stu-id="7f9a3-160">-VaultId</span></span>
<span data-ttu-id="7f9a3-161">ARM ИД хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="7f9a3-161">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f9a3-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f9a3-162">CommonParameters</span></span>
<span data-ttu-id="7f9a3-163">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f9a3-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f9a3-164">Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f9a3-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f9a3-165">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7f9a3-165">INPUTS</span></span>

### <span data-ttu-id="7f9a3-166">System.String</span><span class="sxs-lookup"><span data-stu-id="7f9a3-166">System.String</span></span>

## <span data-ttu-id="7f9a3-167">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7f9a3-167">OUTPUTS</span></span>

### <span data-ttu-id="7f9a3-168">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="7f9a3-168">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="7f9a3-169">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7f9a3-169">NOTES</span></span>

## <span data-ttu-id="7f9a3-170">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7f9a3-170">RELATED LINKS</span></span>


[<span data-ttu-id="7f9a3-171">Stop-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="7f9a3-171">Stop-AzRecoveryServicesBackupJob</span></span>](./Stop-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="7f9a3-172">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="7f9a3-172">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)


