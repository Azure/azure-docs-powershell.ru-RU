---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 623acc7d96fc6c3dc4f1496f42a53bf276f8e778
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079378"
---
# <span data-ttu-id="90738-101">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="90738-101">Get-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="90738-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="90738-102">SYNOPSIS</span></span>

<span data-ttu-id="90738-103">Получает задания резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="90738-103">Gets Backup jobs.</span></span>

## <span data-ttu-id="90738-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="90738-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90738-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="90738-105">DESCRIPTION</span></span>

<span data-ttu-id="90738-106">Командлет **Get-AzRecoveryServicesBackupJob** получает задания резервного копирования Azure для определенного хранилища.</span><span class="sxs-lookup"><span data-stu-id="90738-106">The **Get-AzRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>
<span data-ttu-id="90738-107">Задайте контекст хранилища с помощью параметра-VaultId.</span><span class="sxs-lookup"><span data-stu-id="90738-107">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="90738-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="90738-108">EXAMPLES</span></span>

### <span data-ttu-id="90738-109">Пример 1: получение всех выполняемых заданий</span><span class="sxs-lookup"><span data-stu-id="90738-109">Example 1: Get all in-progress jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Joblist = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> $Joblist[0]

WorkloadName     Operation            Status               StartTime                 EndTime
------------     ---------            ------               ---------                 -------
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="90738-110">Первая команда получает состояние выполняемых заданий в виде массива, а затем сохраняет его в переменной $Joblist.</span><span class="sxs-lookup"><span data-stu-id="90738-110">The first command gets status of an in-progress jobs as an array, and then stores it in the $Joblist variable.</span></span>
<span data-ttu-id="90738-111">Вторая команда отображает первый элемент в массиве $Joblist.</span><span class="sxs-lookup"><span data-stu-id="90738-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="90738-112">Пример 2: получение всех невыполненных заданий за последние 7 дней</span><span class="sxs-lookup"><span data-stu-id="90738-112">Example 2: Get all failed jobs in the last 7 days</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed -VaultId $vault.ID
```

<span data-ttu-id="90738-113">Эта команда возвращает задания с ошибкой за последнюю неделю в хранилище.</span><span class="sxs-lookup"><span data-stu-id="90738-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="90738-114">Параметр *from* указывает время, семь дней в прошлом, указанное в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="90738-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="90738-115">В команде не указывается значение параметра " *Кому* ".</span><span class="sxs-lookup"><span data-stu-id="90738-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="90738-116">Таким образом, используется значение по умолчанию для текущего времени.</span><span class="sxs-lookup"><span data-stu-id="90738-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="90738-117">Пример 3: получение выполняющегося задания и ожидание завершения</span><span class="sxs-lookup"><span data-stu-id="90738-117">Example 3: Get an in-progress job and wait for completion</span></span>

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

<span data-ttu-id="90738-118">Этот сценарий опрашивает первое задание, которое выполняется в данный момент, пока задание не будет завершено.</span><span class="sxs-lookup"><span data-stu-id="90738-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

<span data-ttu-id="90738-119">Примечание. Вы можете использовать командлет **Wait-AzRecoveryServicesBackupJob** , чтобы дождаться завершения задания резервного копирования Azure вместо цикла while.</span><span class="sxs-lookup"><span data-stu-id="90738-119">Note: You can use **Wait-AzRecoveryServicesBackupJob** cmdlet to wait for an Azure Backup job to finish instead of While loop.</span></span>

### <span data-ttu-id="90738-120">Пример 4: получение всех заданий AzureVM за последние 2 дня, которые успешно завершили работу</span><span class="sxs-lookup"><span data-stu-id="90738-120">Example 4: Get all AzureVM jobs in last 2 days which finished successfully</span></span>

```powershell
$vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
$Jobs = Get-AzRecoveryServicesBackupJob  -VaultId $vault.ID  -Status Completed -From (Get-Date).AddDays(-2).ToUniversalTime() -BackupManagementType AzureVM
```
<span data-ttu-id="90738-121">Первый командлет извлекает объект хранилища.</span><span class="sxs-lookup"><span data-stu-id="90738-121">First cmdlet fetches the vault object.</span></span> <span data-ttu-id="90738-122">Второй командлет хранит все задания AzureVM в заданном хранилище, завершенные за последние 2 дня, чтобы $jobs.</span><span class="sxs-lookup"><span data-stu-id="90738-122">Second cmdlet stores all the AzureVM jobs in the given vault which completed in last 2 days to $jobs.</span></span> <span data-ttu-id="90738-123">Измените значение параметра BackupManagementType на MAB, чтобы получить MAB задания агента.</span><span class="sxs-lookup"><span data-stu-id="90738-123">Change the value of BackupManagementType parameter to MAB in order to fetch MAB agent jobs.</span></span>

## <span data-ttu-id="90738-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="90738-124">PARAMETERS</span></span>

### <span data-ttu-id="90738-125">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="90738-125">-BackupManagementType</span></span>

<span data-ttu-id="90738-126">Класс защищаемых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="90738-126">The class of resources being protected.</span></span> <span data-ttu-id="90738-127">В настоящее время для этого командлета поддерживаются следующие значения: AzureVM, AzureStorage, AzureWorkload, MAB.</span><span class="sxs-lookup"><span data-stu-id="90738-127">Currently the values supported for this cmdlet are AzureVM, AzureStorage, AzureWorkload, MAB.</span></span>

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

### <span data-ttu-id="90738-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90738-128">-DefaultProfile</span></span>

<span data-ttu-id="90738-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="90738-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90738-130">-From</span><span class="sxs-lookup"><span data-stu-id="90738-130">-From</span></span>

<span data-ttu-id="90738-131">Задает начало в качестве объекта **DateTime** для диапазона времени для задач, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="90738-131">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="90738-132">Чтобы получить объект **DateTime** , используйте командлет **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="90738-132">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="90738-133">Чтобы получить дополнительные сведения о объектах **DateTime** , введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="90738-133">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="90738-134">Используйте формат UTC для дат.</span><span class="sxs-lookup"><span data-stu-id="90738-134">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="90738-135">-Job</span><span class="sxs-lookup"><span data-stu-id="90738-135">-Job</span></span>

<span data-ttu-id="90738-136">Указывает задание, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="90738-136">Specifies the job to get.</span></span>

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

### <span data-ttu-id="90738-137">-JobId</span><span class="sxs-lookup"><span data-stu-id="90738-137">-JobId</span></span>

<span data-ttu-id="90738-138">Указывает идентификатор задания, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="90738-138">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="90738-139">Идентификатор — это свойство JobId объекта **Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. JobBase** .</span><span class="sxs-lookup"><span data-stu-id="90738-139">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

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

### <span data-ttu-id="90738-140">-Эксплуатация</span><span class="sxs-lookup"><span data-stu-id="90738-140">-Operation</span></span>

<span data-ttu-id="90738-141">Указывает операцию заданий, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="90738-141">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="90738-142">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="90738-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="90738-143">Копирование</span><span class="sxs-lookup"><span data-stu-id="90738-143">Backup</span></span>
- <span data-ttu-id="90738-144">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="90738-144">ConfigureBackup</span></span>
- <span data-ttu-id="90738-145">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="90738-145">DeleteBackupData</span></span>
- <span data-ttu-id="90738-146">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="90738-146">DisableBackup</span></span>
- <span data-ttu-id="90738-147">Восстановление</span><span class="sxs-lookup"><span data-stu-id="90738-147">Restore</span></span>
- <span data-ttu-id="90738-148">BackupDataMove</span><span class="sxs-lookup"><span data-stu-id="90738-148">BackupDataMove</span></span>

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

### <span data-ttu-id="90738-149">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="90738-149">-Status</span></span>

<span data-ttu-id="90738-150">Указывает состояние заданий, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="90738-150">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="90738-151">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="90738-151">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="90738-152">Ход выполнения</span><span class="sxs-lookup"><span data-stu-id="90738-152">InProgress</span></span>
- <span data-ttu-id="90738-153">Ошибкой</span><span class="sxs-lookup"><span data-stu-id="90738-153">Failed</span></span>
- <span data-ttu-id="90738-154">Отменен</span><span class="sxs-lookup"><span data-stu-id="90738-154">Cancelled</span></span>
- <span data-ttu-id="90738-155">Отмена</span><span class="sxs-lookup"><span data-stu-id="90738-155">Cancelling</span></span>
- <span data-ttu-id="90738-156">Completed</span><span class="sxs-lookup"><span data-stu-id="90738-156">Completed</span></span>
- <span data-ttu-id="90738-157">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="90738-157">CompletedWithWarnings</span></span>

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

### <span data-ttu-id="90738-158">-To</span><span class="sxs-lookup"><span data-stu-id="90738-158">-To</span></span>

<span data-ttu-id="90738-159">Задает конечный объект в качестве объекта **DateTime** из диапазона времени для задач, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="90738-159">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="90738-160">Значение по умолчанию — текущее системное время.</span><span class="sxs-lookup"><span data-stu-id="90738-160">The default value is the current system time.</span></span>
<span data-ttu-id="90738-161">Если указать этот параметр, необходимо также указать параметр **-from** .</span><span class="sxs-lookup"><span data-stu-id="90738-161">If you specify this parameter, you must also specify the **-From** parameter.</span></span>
<span data-ttu-id="90738-162">Используйте формат UTC для дат.</span><span class="sxs-lookup"><span data-stu-id="90738-162">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="90738-163">-VaultId</span><span class="sxs-lookup"><span data-stu-id="90738-163">-VaultId</span></span>

<span data-ttu-id="90738-164">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="90738-164">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="90738-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90738-165">CommonParameters</span></span>
<span data-ttu-id="90738-166">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="90738-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90738-167">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90738-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90738-168">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="90738-168">INPUTS</span></span>

### <span data-ttu-id="90738-169">System. String</span><span class="sxs-lookup"><span data-stu-id="90738-169">System.String</span></span>

## <span data-ttu-id="90738-170">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="90738-170">OUTPUTS</span></span>

### <span data-ttu-id="90738-171">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="90738-171">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="90738-172">Пуск</span><span class="sxs-lookup"><span data-stu-id="90738-172">NOTES</span></span>

## <span data-ttu-id="90738-173">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="90738-173">RELATED LINKS</span></span>

[<span data-ttu-id="90738-174">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="90738-174">Get-AzRecoveryServicesBackupJobDetail</span></span>](./Get-AzRecoveryServicesBackupJobDetail.md)

[<span data-ttu-id="90738-175">Остановить-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="90738-175">Stop-AzRecoveryServicesBackupJob</span></span>](./Stop-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="90738-176">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="90738-176">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)
