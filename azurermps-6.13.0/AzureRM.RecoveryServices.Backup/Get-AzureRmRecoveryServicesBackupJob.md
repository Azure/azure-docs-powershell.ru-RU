---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: 0ed0ed82c1f2c030ab10fc6a96d1582fdb34b7d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567696"
---
# <span data-ttu-id="92d5e-101">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="92d5e-101">Get-AzureRmRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="92d5e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="92d5e-102">SYNOPSIS</span></span>
<span data-ttu-id="92d5e-103">Получает задания резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="92d5e-103">Gets Backup jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92d5e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="92d5e-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92d5e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="92d5e-105">DESCRIPTION</span></span>
<span data-ttu-id="92d5e-106">Командлет **Get-AzureRmRecoveryServicesBackupJob** получает задания резервного копирования Azure для определенного хранилища.</span><span class="sxs-lookup"><span data-stu-id="92d5e-106">The **Get-AzureRmRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>
<span data-ttu-id="92d5e-107">Настройте контекст хранилища с помощью командлета Set-AzureRmRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="92d5e-107">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="92d5e-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="92d5e-108">EXAMPLES</span></span>

### <span data-ttu-id="92d5e-109">Пример 1: получение всех выполняемых заданий</span><span class="sxs-lookup"><span data-stu-id="92d5e-109">Example 1: Get all in-progress jobs</span></span>
```
PS C:\>$Joblist = Get-AzureRMRecoveryservicesBackupJob -Status Inprogress
PS C:\> $Joblist[0]
WorkloadName     Operation            Status               StartTime                 EndTime                                             
------------     ---------            ------               ---------                 -------                                             
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="92d5e-110">Первая команда получает состояние выполняющегося задания в виде массива, а затем сохраняет его в переменной $Joblist.</span><span class="sxs-lookup"><span data-stu-id="92d5e-110">The first command gets status of an in-progress job as an array, and then stores it in the $Joblist variable.</span></span>
<span data-ttu-id="92d5e-111">Вторая команда отображает первый элемент в массиве $Joblist.</span><span class="sxs-lookup"><span data-stu-id="92d5e-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="92d5e-112">Пример 2: получение всех невыполненных заданий за последние 7 дней</span><span class="sxs-lookup"><span data-stu-id="92d5e-112">Example 2: Get all failed jobs in the last 7 days</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed
```

<span data-ttu-id="92d5e-113">Эта команда возвращает задания с ошибкой за последнюю неделю в хранилище.</span><span class="sxs-lookup"><span data-stu-id="92d5e-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="92d5e-114">Параметр *from* указывает время, семь дней в прошлом, указанное в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="92d5e-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="92d5e-115">В команде не указывается значение параметра " *Кому* ".</span><span class="sxs-lookup"><span data-stu-id="92d5e-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="92d5e-116">Таким образом, используется значение по умолчанию для текущего времени.</span><span class="sxs-lookup"><span data-stu-id="92d5e-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="92d5e-117">Пример 3: получение выполняющегося задания и ожидание завершения</span><span class="sxs-lookup"><span data-stu-id="92d5e-117">Example 3: Get an in-progress job and wait for completion</span></span>
```
PS C:\> 
$Jobs = Get-AzureRmRecoveryServicesBackupJob -Status InProgress
$Job = $Jobs[0]
    while ( $Job.Status -ne Completed )
    {
       Write-Host "Waiting for completion..."
       Start-Sleep -Seconds 10
       $job = Get-AzureRmBackAzureRmRecoveryServicesBackupJob  -Job $Job
    }
    Write-Host "Done!"
    Waiting for completion... 
    Waiting for completion... 
    Waiting for completion... 
    Done!
```

<span data-ttu-id="92d5e-118">Этот сценарий опрашивает первое задание, которое выполняется в данный момент, пока задание не будет завершено.</span><span class="sxs-lookup"><span data-stu-id="92d5e-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="92d5e-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="92d5e-119">PARAMETERS</span></span>

### <span data-ttu-id="92d5e-120">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="92d5e-120">-BackupManagementType</span></span>
<span data-ttu-id="92d5e-121">Указывает тип управления резервным копированием.</span><span class="sxs-lookup"><span data-stu-id="92d5e-121">Specifies the Backup management type.</span></span>
<span data-ttu-id="92d5e-122">В настоящее время поддерживается только AzureVM, AzureStorage.</span><span class="sxs-lookup"><span data-stu-id="92d5e-122">Currently, only AzureVM, AzureStorage is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92d5e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92d5e-123">-DefaultProfile</span></span>
<span data-ttu-id="92d5e-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="92d5e-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92d5e-125">-From</span><span class="sxs-lookup"><span data-stu-id="92d5e-125">-From</span></span>
<span data-ttu-id="92d5e-126">Задает начало в качестве объекта **DateTime** для диапазона времени для задач, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="92d5e-126">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="92d5e-127">Чтобы получить объект **DateTime** , используйте командлет Get-Date.</span><span class="sxs-lookup"><span data-stu-id="92d5e-127">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="92d5e-128">Чтобы получить дополнительные сведения о объектах **DateTime** , введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="92d5e-128">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="92d5e-129">Используйте формат UTC для дат.</span><span class="sxs-lookup"><span data-stu-id="92d5e-129">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="92d5e-130">-Job</span><span class="sxs-lookup"><span data-stu-id="92d5e-130">-Job</span></span>
<span data-ttu-id="92d5e-131">Указывает имя задания резервного копирования, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="92d5e-131">Specifies the name of the Backup job to get.</span></span>

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

### <span data-ttu-id="92d5e-132">-JobId</span><span class="sxs-lookup"><span data-stu-id="92d5e-132">-JobId</span></span>
<span data-ttu-id="92d5e-133">Указывает идентификатор задания, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="92d5e-133">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="92d5e-134">Идентификатор — это свойство InstanceId объекта **AzureRmRecoveryServicesBackupJob** .</span><span class="sxs-lookup"><span data-stu-id="92d5e-134">The ID is the InstanceId property of an **AzureRmRecoveryServicesBackupJob** object.</span></span>
<span data-ttu-id="92d5e-135">Чтобы получить объект **AzureRmRecoveryServicesBackupJob** , используйте Get-AzureRmRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="92d5e-135">To obtain an **AzureRmRecoveryServicesBackupJob** object, use Get-AzureRmRecoveryServicesBackupJob.</span></span>

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

### <span data-ttu-id="92d5e-136">-Эксплуатация</span><span class="sxs-lookup"><span data-stu-id="92d5e-136">-Operation</span></span>
<span data-ttu-id="92d5e-137">Указывает операцию заданий, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="92d5e-137">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="92d5e-138">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="92d5e-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="92d5e-139">Копирование</span><span class="sxs-lookup"><span data-stu-id="92d5e-139">Backup</span></span>
- <span data-ttu-id="92d5e-140">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="92d5e-140">ConfigureBackup</span></span>
- <span data-ttu-id="92d5e-141">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="92d5e-141">DeleteBackupData</span></span>
- <span data-ttu-id="92d5e-142">Отменить</span><span class="sxs-lookup"><span data-stu-id="92d5e-142">Register</span></span>
- <span data-ttu-id="92d5e-143">Восстановление</span><span class="sxs-lookup"><span data-stu-id="92d5e-143">Restore</span></span>
- <span data-ttu-id="92d5e-144">Снять защиту</span><span class="sxs-lookup"><span data-stu-id="92d5e-144">UnProtect</span></span>
- <span data-ttu-id="92d5e-145">Отмените регистрацию</span><span class="sxs-lookup"><span data-stu-id="92d5e-145">Unregister</span></span>

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

### <span data-ttu-id="92d5e-146">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="92d5e-146">-Status</span></span>
<span data-ttu-id="92d5e-147">Указывает состояние заданий, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="92d5e-147">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="92d5e-148">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="92d5e-148">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="92d5e-149">Ход выполнения</span><span class="sxs-lookup"><span data-stu-id="92d5e-149">InProgress</span></span>
- <span data-ttu-id="92d5e-150">Ошибкой</span><span class="sxs-lookup"><span data-stu-id="92d5e-150">Failed</span></span>
- <span data-ttu-id="92d5e-151">Отменен</span><span class="sxs-lookup"><span data-stu-id="92d5e-151">Cancelled</span></span>
- <span data-ttu-id="92d5e-152">Отмена</span><span class="sxs-lookup"><span data-stu-id="92d5e-152">Cancelling</span></span>
- <span data-ttu-id="92d5e-153">Completed</span><span class="sxs-lookup"><span data-stu-id="92d5e-153">Completed</span></span>
- <span data-ttu-id="92d5e-154">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="92d5e-154">CompletedWithWarnings</span></span>

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

### <span data-ttu-id="92d5e-155">-To</span><span class="sxs-lookup"><span data-stu-id="92d5e-155">-To</span></span>
<span data-ttu-id="92d5e-156">Задает конечный объект в качестве объекта **DateTime** из диапазона времени для задач, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="92d5e-156">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="92d5e-157">Значение по умолчанию — текущее системное время.</span><span class="sxs-lookup"><span data-stu-id="92d5e-157">The default value is the current system time.</span></span>
<span data-ttu-id="92d5e-158">Если указать этот параметр, необходимо также указать параметр *from* .</span><span class="sxs-lookup"><span data-stu-id="92d5e-158">If you specify this parameter, you must also specify the *From* parameter.</span></span>
<span data-ttu-id="92d5e-159">Используйте формат UTC для дат.</span><span class="sxs-lookup"><span data-stu-id="92d5e-159">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="92d5e-160">-VaultId</span><span class="sxs-lookup"><span data-stu-id="92d5e-160">-VaultId</span></span>
<span data-ttu-id="92d5e-161">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="92d5e-161">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="92d5e-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92d5e-162">CommonParameters</span></span>
<span data-ttu-id="92d5e-163">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="92d5e-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92d5e-164">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92d5e-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92d5e-165">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="92d5e-165">INPUTS</span></span>

### <span data-ttu-id="92d5e-166">System. String</span><span class="sxs-lookup"><span data-stu-id="92d5e-166">System.String</span></span>
<span data-ttu-id="92d5e-167">Параметры: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="92d5e-167">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="92d5e-168">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="92d5e-168">OUTPUTS</span></span>

### <span data-ttu-id="92d5e-169">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="92d5e-169">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="92d5e-170">Пуск</span><span class="sxs-lookup"><span data-stu-id="92d5e-170">NOTES</span></span>

## <span data-ttu-id="92d5e-171">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="92d5e-171">RELATED LINKS</span></span>

[<span data-ttu-id="92d5e-172">Get-AzureRmRecoveryServicesBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="92d5e-172">Get-AzureRmRecoveryServicesBackupJobDetails</span></span>](./Get-AzureRmRecoveryServicesBackupJobDetails.md)

[<span data-ttu-id="92d5e-173">Остановить-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="92d5e-173">Stop-AzureRmRecoveryServicesBackupJob</span></span>](./Stop-AzureRmRecoveryServicesBackupJob.md)

[<span data-ttu-id="92d5e-174">Wait-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="92d5e-174">Wait-AzureRmRecoveryServicesBackupJob</span></span>](./Wait-AzureRmRecoveryServicesBackupJob.md)


