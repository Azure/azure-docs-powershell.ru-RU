---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 21498e13490b22b58621e2100dcc885442db7607
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729706"
---
# <span data-ttu-id="954b9-101">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="954b9-101">Get-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="954b9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="954b9-102">SYNOPSIS</span></span>
<span data-ttu-id="954b9-103">Получает задания резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="954b9-103">Gets Backup jobs.</span></span>

## <span data-ttu-id="954b9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="954b9-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="954b9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="954b9-105">DESCRIPTION</span></span>
<span data-ttu-id="954b9-106">Командлет **Get-AzRecoveryServicesBackupJob** получает задания резервного копирования Azure для определенного хранилища.</span><span class="sxs-lookup"><span data-stu-id="954b9-106">The **Get-AzRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>
<span data-ttu-id="954b9-107">Настройте контекст хранилища с помощью командлета Set-AzRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="954b9-107">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="954b9-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="954b9-108">EXAMPLES</span></span>

### <span data-ttu-id="954b9-109">Пример 1: получение всех выполняемых заданий</span><span class="sxs-lookup"><span data-stu-id="954b9-109">Example 1: Get all in-progress jobs</span></span>
```
PS C:\>$Joblist = Get-AzRecoveryservicesBackupJob -Status Inprogress
PS C:\> $Joblist[0]
WorkloadName     Operation            Status               StartTime                 EndTime                                             
------------     ---------            ------               ---------                 -------                                             
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="954b9-110">Первая команда получает состояние выполняющегося задания в виде массива, а затем сохраняет его в переменной $Joblist.</span><span class="sxs-lookup"><span data-stu-id="954b9-110">The first command gets status of an in-progress job as an array, and then stores it in the $Joblist variable.</span></span>
<span data-ttu-id="954b9-111">Вторая команда отображает первый элемент в массиве $Joblist.</span><span class="sxs-lookup"><span data-stu-id="954b9-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="954b9-112">Пример 2: получение всех невыполненных заданий за последние 7 дней</span><span class="sxs-lookup"><span data-stu-id="954b9-112">Example 2: Get all failed jobs in the last 7 days</span></span>
```
PS C:\>Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed
```

<span data-ttu-id="954b9-113">Эта команда возвращает задания с ошибкой за последнюю неделю в хранилище.</span><span class="sxs-lookup"><span data-stu-id="954b9-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="954b9-114">Параметр *from* указывает время, семь дней в прошлом, указанное в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="954b9-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="954b9-115">В команде не указывается значение параметра " *Кому* ".</span><span class="sxs-lookup"><span data-stu-id="954b9-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="954b9-116">Таким образом, используется значение по умолчанию для текущего времени.</span><span class="sxs-lookup"><span data-stu-id="954b9-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="954b9-117">Пример 3: получение выполняющегося задания и ожидание завершения</span><span class="sxs-lookup"><span data-stu-id="954b9-117">Example 3: Get an in-progress job and wait for completion</span></span>
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

<span data-ttu-id="954b9-118">Этот сценарий опрашивает первое задание, которое выполняется в данный момент, пока задание не будет завершено.</span><span class="sxs-lookup"><span data-stu-id="954b9-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="954b9-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="954b9-119">PARAMETERS</span></span>

### <span data-ttu-id="954b9-120">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="954b9-120">-BackupManagementType</span></span>
<span data-ttu-id="954b9-121">Указывает тип управления резервным копированием.</span><span class="sxs-lookup"><span data-stu-id="954b9-121">Specifies the Backup management type.</span></span>
<span data-ttu-id="954b9-122">В настоящее время поддерживается только AzureVM, AzureStorage.</span><span class="sxs-lookup"><span data-stu-id="954b9-122">Currently, only AzureVM, AzureStorage is supported.</span></span>

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

### <span data-ttu-id="954b9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="954b9-123">-DefaultProfile</span></span>
<span data-ttu-id="954b9-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="954b9-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="954b9-125">-From</span><span class="sxs-lookup"><span data-stu-id="954b9-125">-From</span></span>
<span data-ttu-id="954b9-126">Задает начало в качестве объекта **DateTime** для диапазона времени для задач, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="954b9-126">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="954b9-127">Чтобы получить объект **DateTime** , используйте командлет Get-Date.</span><span class="sxs-lookup"><span data-stu-id="954b9-127">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="954b9-128">Чтобы получить дополнительные сведения о объектах **DateTime** , введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="954b9-128">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="954b9-129">Используйте формат UTC для дат.</span><span class="sxs-lookup"><span data-stu-id="954b9-129">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="954b9-130">-Job</span><span class="sxs-lookup"><span data-stu-id="954b9-130">-Job</span></span>
<span data-ttu-id="954b9-131">Указывает имя задания резервного копирования, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="954b9-131">Specifies the name of the Backup job to get.</span></span>

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

### <span data-ttu-id="954b9-132">-JobId</span><span class="sxs-lookup"><span data-stu-id="954b9-132">-JobId</span></span>
<span data-ttu-id="954b9-133">Указывает идентификатор задания, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="954b9-133">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="954b9-134">Идентификатор — это свойство InstanceId объекта **AzureRmRecoveryServicesBackupJob** .</span><span class="sxs-lookup"><span data-stu-id="954b9-134">The ID is the InstanceId property of an **AzureRmRecoveryServicesBackupJob** object.</span></span>
<span data-ttu-id="954b9-135">Чтобы получить объект **AzureRmRecoveryServicesBackupJob** , используйте Get-AzRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="954b9-135">To obtain an **AzureRmRecoveryServicesBackupJob** object, use Get-AzRecoveryServicesBackupJob.</span></span>

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

### <span data-ttu-id="954b9-136">-Эксплуатация</span><span class="sxs-lookup"><span data-stu-id="954b9-136">-Operation</span></span>
<span data-ttu-id="954b9-137">Указывает операцию заданий, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="954b9-137">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="954b9-138">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="954b9-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="954b9-139">Копирование</span><span class="sxs-lookup"><span data-stu-id="954b9-139">Backup</span></span>
- <span data-ttu-id="954b9-140">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="954b9-140">ConfigureBackup</span></span>
- <span data-ttu-id="954b9-141">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="954b9-141">DeleteBackupData</span></span>
- <span data-ttu-id="954b9-142">Отменить</span><span class="sxs-lookup"><span data-stu-id="954b9-142">Register</span></span>
- <span data-ttu-id="954b9-143">Восстановление</span><span class="sxs-lookup"><span data-stu-id="954b9-143">Restore</span></span>
- <span data-ttu-id="954b9-144">Снять защиту</span><span class="sxs-lookup"><span data-stu-id="954b9-144">UnProtect</span></span>
- <span data-ttu-id="954b9-145">Отмените регистрацию</span><span class="sxs-lookup"><span data-stu-id="954b9-145">Unregister</span></span>

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

### <span data-ttu-id="954b9-146">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="954b9-146">-Status</span></span>
<span data-ttu-id="954b9-147">Указывает состояние заданий, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="954b9-147">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="954b9-148">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="954b9-148">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="954b9-149">Ход выполнения</span><span class="sxs-lookup"><span data-stu-id="954b9-149">InProgress</span></span>
- <span data-ttu-id="954b9-150">Ошибкой</span><span class="sxs-lookup"><span data-stu-id="954b9-150">Failed</span></span>
- <span data-ttu-id="954b9-151">Отменен</span><span class="sxs-lookup"><span data-stu-id="954b9-151">Cancelled</span></span>
- <span data-ttu-id="954b9-152">Отмена</span><span class="sxs-lookup"><span data-stu-id="954b9-152">Cancelling</span></span>
- <span data-ttu-id="954b9-153">Completed</span><span class="sxs-lookup"><span data-stu-id="954b9-153">Completed</span></span>
- <span data-ttu-id="954b9-154">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="954b9-154">CompletedWithWarnings</span></span>

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

### <span data-ttu-id="954b9-155">-To</span><span class="sxs-lookup"><span data-stu-id="954b9-155">-To</span></span>
<span data-ttu-id="954b9-156">Задает конечный объект в качестве объекта **DateTime** из диапазона времени для задач, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="954b9-156">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="954b9-157">Значение по умолчанию — текущее системное время.</span><span class="sxs-lookup"><span data-stu-id="954b9-157">The default value is the current system time.</span></span>
<span data-ttu-id="954b9-158">Если указать этот параметр, необходимо также указать параметр *from* .</span><span class="sxs-lookup"><span data-stu-id="954b9-158">If you specify this parameter, you must also specify the *From* parameter.</span></span>
<span data-ttu-id="954b9-159">Используйте формат UTC для дат.</span><span class="sxs-lookup"><span data-stu-id="954b9-159">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="954b9-160">-VaultId</span><span class="sxs-lookup"><span data-stu-id="954b9-160">-VaultId</span></span>
<span data-ttu-id="954b9-161">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="954b9-161">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="954b9-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="954b9-162">CommonParameters</span></span>
<span data-ttu-id="954b9-163">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="954b9-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="954b9-164">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="954b9-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="954b9-165">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="954b9-165">INPUTS</span></span>

### <span data-ttu-id="954b9-166">System. String</span><span class="sxs-lookup"><span data-stu-id="954b9-166">System.String</span></span>

## <span data-ttu-id="954b9-167">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="954b9-167">OUTPUTS</span></span>

### <span data-ttu-id="954b9-168">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="954b9-168">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="954b9-169">Пуск</span><span class="sxs-lookup"><span data-stu-id="954b9-169">NOTES</span></span>

## <span data-ttu-id="954b9-170">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="954b9-170">RELATED LINKS</span></span>

[<span data-ttu-id="954b9-171">Get-AzRecoveryServicesBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="954b9-171">Get-AzRecoveryServicesBackupJobDetails</span></span>](./Get-AzRecoveryServicesBackupJobDetails.md)

[<span data-ttu-id="954b9-172">Остановить-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="954b9-172">Stop-AzRecoveryServicesBackupJob</span></span>](./Stop-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="954b9-173">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="954b9-173">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)


