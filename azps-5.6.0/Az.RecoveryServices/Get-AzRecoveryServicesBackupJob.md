---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 011b27cfff166173d485636a1e8890d917484651
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984243"
---
# <span data-ttu-id="0133d-101">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="0133d-101">Get-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="0133d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0133d-102">SYNOPSIS</span></span>

<span data-ttu-id="0133d-103">Возвращает задания резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="0133d-103">Gets Backup jobs.</span></span>

## <span data-ttu-id="0133d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0133d-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
  [-UseSecondaryRegion] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0133d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0133d-105">DESCRIPTION</span></span>

<span data-ttu-id="0133d-106">Чтобы получить задания резервного копирования для определенного хранилища, можно получить задания резервного копирования Azure с использованием **cmdlet Get-AzRecoveryServicesBackupJob.**</span><span class="sxs-lookup"><span data-stu-id="0133d-106">The **Get-AzRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>
<span data-ttu-id="0133d-107">Задать контекст хранилища с помощью параметра -VaultId.</span><span class="sxs-lookup"><span data-stu-id="0133d-107">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="0133d-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0133d-108">EXAMPLES</span></span>

### <span data-ttu-id="0133d-109">Пример 1. Работа со всеми заданиями</span><span class="sxs-lookup"><span data-stu-id="0133d-109">Example 1: Get all in-progress jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Joblist = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> $Joblist[0]

WorkloadName     Operation            Status               StartTime                 EndTime
------------     ---------            ------               ---------                 -------
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="0133d-110">Первая команда получает состояние выполнения заданий как массив, а затем сохраняет его в $Joblist переменной.</span><span class="sxs-lookup"><span data-stu-id="0133d-110">The first command gets status of an in-progress jobs as an array, and then stores it in the $Joblist variable.</span></span>
<span data-ttu-id="0133d-111">Вторая команда отображает первый элемент в $Joblist массиве.</span><span class="sxs-lookup"><span data-stu-id="0133d-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="0133d-112">Пример 2. Получить все сбойные задания за последние 7 дней</span><span class="sxs-lookup"><span data-stu-id="0133d-112">Example 2: Get all failed jobs in the last 7 days</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed -VaultId $vault.ID
```

<span data-ttu-id="0133d-113">Эта команда получает сбой заданий за последнюю неделю в хранилище.</span><span class="sxs-lookup"><span data-stu-id="0133d-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="0133d-114">Параметр *From* определяет время, прошедшее семь дней, указанное в UTC.</span><span class="sxs-lookup"><span data-stu-id="0133d-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="0133d-115">Эта команда не указывает значение параметра *To.*</span><span class="sxs-lookup"><span data-stu-id="0133d-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="0133d-116">Поэтому в нем используется значение по умолчанию для текущего времени.</span><span class="sxs-lookup"><span data-stu-id="0133d-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="0133d-117">Пример 3. Получить задание и дождаться завершения</span><span class="sxs-lookup"><span data-stu-id="0133d-117">Example 3: Get an in-progress job and wait for completion</span></span>

```powershell
$vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
$Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
$Job = $Jobs[0]
While ( $Job.Status -ne Completed ) {
    Write-Host -Object "Waiting for completion..."
    Start-Sleep -Seconds 10
    $Job = Get-AzRecoveryServicesBackupJob -Job $Job -VaultId $vault.ID
}
Write-Host -Object "Done!"

Waiting for completion... 
Waiting for completion... 
Waiting for completion... 
Done!
```

<span data-ttu-id="0133d-118">Этот сценарий оповестит первое задание, которое в настоящее время находится в процессе выполнения, пока задание не будет завершено.</span><span class="sxs-lookup"><span data-stu-id="0133d-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

<span data-ttu-id="0133d-119">Примечание. Чтобы дождаться завершения задания резервного копирования Azure, а не цикла, можно использовать для этого cmdlet **Wait-AzRecoveryServicesBackupJob.**</span><span class="sxs-lookup"><span data-stu-id="0133d-119">Note: You can use **Wait-AzRecoveryServicesBackupJob** cmdlet to wait for an Azure Backup job to finish instead of While loop.</span></span>

### <span data-ttu-id="0133d-120">Пример 4. Все задания AzureVM за последние 2 дня, завершенные успешно</span><span class="sxs-lookup"><span data-stu-id="0133d-120">Example 4: Get all AzureVM jobs in last 2 days which finished successfully</span></span>

```powershell
$vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
$Jobs = Get-AzRecoveryServicesBackupJob  -VaultId $vault.ID  -Status Completed -From (Get-Date).AddDays(-2).ToUniversalTime() -BackupManagementType AzureVM
```
<span data-ttu-id="0133d-121">Первый cmdlet извлекает объект хранилища.</span><span class="sxs-lookup"><span data-stu-id="0133d-121">First cmdlet fetches the vault object.</span></span> <span data-ttu-id="0133d-122">Второй cmdlet хранит все задания AzureVM в этом хранилище, которые были выполнены за последние 2 дня, чтобы $jobs.</span><span class="sxs-lookup"><span data-stu-id="0133d-122">Second cmdlet stores all the AzureVM jobs in the given vault which completed in last 2 days to $jobs.</span></span> <span data-ttu-id="0133d-123">Измените значение параметра BackupManagementType на MAB, чтобы получить задания агентов MAB.</span><span class="sxs-lookup"><span data-stu-id="0133d-123">Change the value of BackupManagementType parameter to MAB in order to fetch MAB agent jobs.</span></span>

## <span data-ttu-id="0133d-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0133d-124">PARAMETERS</span></span>

### <span data-ttu-id="0133d-125">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="0133d-125">-BackupManagementType</span></span>

<span data-ttu-id="0133d-126">Класс защищенных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0133d-126">The class of resources being protected.</span></span> <span data-ttu-id="0133d-127">В настоящее время для этого командлета поддерживаются такие значения: AzureVM, AzureStorage, AzureWorkload, MAB.</span><span class="sxs-lookup"><span data-stu-id="0133d-127">Currently the values supported for this cmdlet are AzureVM, AzureStorage, AzureWorkload, MAB.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureStorage, AzureWorkload, MAB

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0133d-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0133d-128">-DefaultProfile</span></span>

<span data-ttu-id="0133d-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0133d-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0133d-130">-From</span><span class="sxs-lookup"><span data-stu-id="0133d-130">-From</span></span>

<span data-ttu-id="0133d-131">Начало в качестве объекта **даты и времени** для диапазона времени для заданий, которые получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0133d-131">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="0133d-132">Чтобы получить объект **даты и времени,** используйте cmdlet **Get-Date.**</span><span class="sxs-lookup"><span data-stu-id="0133d-132">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="0133d-133">Чтобы получить дополнительные сведения об **объектах даты и времени,** введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="0133d-133">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="0133d-134">Для дат используйте формат UTC.</span><span class="sxs-lookup"><span data-stu-id="0133d-134">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="0133d-135">-Job</span><span class="sxs-lookup"><span data-stu-id="0133d-135">-Job</span></span>

<span data-ttu-id="0133d-136">Задание, которую нужно получить.</span><span class="sxs-lookup"><span data-stu-id="0133d-136">Specifies the job to get.</span></span>

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

### <span data-ttu-id="0133d-137">-JobId</span><span class="sxs-lookup"><span data-stu-id="0133d-137">-JobId</span></span>

<span data-ttu-id="0133d-138">Определяет код задания, которое получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0133d-138">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="0133d-139">Код — это свойство JobId объекта **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase.**</span><span class="sxs-lookup"><span data-stu-id="0133d-139">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

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

### <span data-ttu-id="0133d-140">-Operation</span><span class="sxs-lookup"><span data-stu-id="0133d-140">-Operation</span></span>

<span data-ttu-id="0133d-141">Указывает операцию заданий, которые получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0133d-141">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="0133d-142">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="0133d-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0133d-143">Резервное копирование</span><span class="sxs-lookup"><span data-stu-id="0133d-143">Backup</span></span>
- <span data-ttu-id="0133d-144">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="0133d-144">ConfigureBackup</span></span>
- <span data-ttu-id="0133d-145">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="0133d-145">DeleteBackupData</span></span>
- <span data-ttu-id="0133d-146">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="0133d-146">DisableBackup</span></span>
- <span data-ttu-id="0133d-147">"Восстановить"</span><span class="sxs-lookup"><span data-stu-id="0133d-147">Restore</span></span>
- <span data-ttu-id="0133d-148">BackupDataMove</span><span class="sxs-lookup"><span data-stu-id="0133d-148">BackupDataMove</span></span>

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

### <span data-ttu-id="0133d-149">-Status</span><span class="sxs-lookup"><span data-stu-id="0133d-149">-Status</span></span>

<span data-ttu-id="0133d-150">Указывает состояние заданий, которые получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0133d-150">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="0133d-151">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="0133d-151">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0133d-152">InProgress</span><span class="sxs-lookup"><span data-stu-id="0133d-152">InProgress</span></span>
- <span data-ttu-id="0133d-153">Сбой</span><span class="sxs-lookup"><span data-stu-id="0133d-153">Failed</span></span>
- <span data-ttu-id="0133d-154">Отменено</span><span class="sxs-lookup"><span data-stu-id="0133d-154">Cancelled</span></span>
- <span data-ttu-id="0133d-155">Отмена</span><span class="sxs-lookup"><span data-stu-id="0133d-155">Cancelling</span></span>
- <span data-ttu-id="0133d-156">Завершено</span><span class="sxs-lookup"><span data-stu-id="0133d-156">Completed</span></span>
- <span data-ttu-id="0133d-157">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="0133d-157">CompletedWithWarnings</span></span>

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

### <span data-ttu-id="0133d-158">-To</span><span class="sxs-lookup"><span data-stu-id="0133d-158">-To</span></span>

<span data-ttu-id="0133d-159">Окончание в качестве объекта **даты и времени** для диапазона времени для заданий, которые получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0133d-159">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="0133d-160">Значением по умолчанию является текущее системное время.</span><span class="sxs-lookup"><span data-stu-id="0133d-160">The default value is the current system time.</span></span>
<span data-ttu-id="0133d-161">Если этот параметр указан, необходимо также указать параметр **-From.**</span><span class="sxs-lookup"><span data-stu-id="0133d-161">If you specify this parameter, you must also specify the **-From** parameter.</span></span>
<span data-ttu-id="0133d-162">Для дат используйте формат UTC.</span><span class="sxs-lookup"><span data-stu-id="0133d-162">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="0133d-163">-VaultId</span><span class="sxs-lookup"><span data-stu-id="0133d-163">-VaultId</span></span>

<span data-ttu-id="0133d-164">ARM ИД хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="0133d-164">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="0133d-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0133d-165">CommonParameters</span></span>
<span data-ttu-id="0133d-166">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0133d-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0133d-167">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0133d-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0133d-168">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0133d-168">INPUTS</span></span>

### <span data-ttu-id="0133d-169">System.String</span><span class="sxs-lookup"><span data-stu-id="0133d-169">System.String</span></span>

## <span data-ttu-id="0133d-170">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0133d-170">OUTPUTS</span></span>

### <span data-ttu-id="0133d-171">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="0133d-171">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="0133d-172">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0133d-172">NOTES</span></span>

## <span data-ttu-id="0133d-173">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0133d-173">RELATED LINKS</span></span>

[<span data-ttu-id="0133d-174">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="0133d-174">Get-AzRecoveryServicesBackupJobDetail</span></span>](./Get-AzRecoveryServicesBackupJobDetail.md)

[<span data-ttu-id="0133d-175">Stop-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="0133d-175">Stop-AzRecoveryServicesBackupJob</span></span>](./Stop-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="0133d-176">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="0133d-176">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)
