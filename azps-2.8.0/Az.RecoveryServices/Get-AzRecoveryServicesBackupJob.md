---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: cc23d8535e7aaca656379811121ed09bad2f64bc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904938"
---
# <span data-ttu-id="a4c59-101">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="a4c59-101">Get-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="a4c59-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a4c59-102">SYNOPSIS</span></span>

<span data-ttu-id="a4c59-103">Получает задания резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="a4c59-103">Gets Backup jobs.</span></span>

## <span data-ttu-id="a4c59-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a4c59-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4c59-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4c59-105">DESCRIPTION</span></span>

<span data-ttu-id="a4c59-106">Командлет **Get-AzRecoveryServicesBackupJob** получает задания резервного копирования Azure для определенного хранилища.</span><span class="sxs-lookup"><span data-stu-id="a4c59-106">The **Get-AzRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>
<span data-ttu-id="a4c59-107">Задайте контекст хранилища с помощью параметра-VaultId.</span><span class="sxs-lookup"><span data-stu-id="a4c59-107">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="a4c59-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a4c59-108">EXAMPLES</span></span>

### <span data-ttu-id="a4c59-109">Пример 1: получение всех выполняемых заданий</span><span class="sxs-lookup"><span data-stu-id="a4c59-109">Example 1: Get all in-progress jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Joblist = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> $Joblist[0]

WorkloadName     Operation            Status               StartTime                 EndTime
------------     ---------            ------               ---------                 -------
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="a4c59-110">Первая команда получает состояние выполняемых заданий в виде массива, а затем сохраняет его в переменной $Joblist.</span><span class="sxs-lookup"><span data-stu-id="a4c59-110">The first command gets status of an in-progress jobs as an array, and then stores it in the $Joblist variable.</span></span>
<span data-ttu-id="a4c59-111">Вторая команда отображает первый элемент в массиве $Joblist.</span><span class="sxs-lookup"><span data-stu-id="a4c59-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="a4c59-112">Пример 2: получение всех невыполненных заданий за последние 7 дней</span><span class="sxs-lookup"><span data-stu-id="a4c59-112">Example 2: Get all failed jobs in the last 7 days</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed -VaultId $vault.ID
```

<span data-ttu-id="a4c59-113">Эта команда возвращает задания с ошибкой за последнюю неделю в хранилище.</span><span class="sxs-lookup"><span data-stu-id="a4c59-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="a4c59-114">Параметр *from* указывает время, семь дней в прошлом, указанное в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="a4c59-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="a4c59-115">В команде не указывается значение параметра " *Кому* ".</span><span class="sxs-lookup"><span data-stu-id="a4c59-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="a4c59-116">Таким образом, используется значение по умолчанию для текущего времени.</span><span class="sxs-lookup"><span data-stu-id="a4c59-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="a4c59-117">Пример 3: получение выполняющегося задания и ожидание завершения</span><span class="sxs-lookup"><span data-stu-id="a4c59-117">Example 3: Get an in-progress job and wait for completion</span></span>

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

<span data-ttu-id="a4c59-118">Этот сценарий опрашивает первое задание, которое выполняется в данный момент, пока задание не будет завершено.</span><span class="sxs-lookup"><span data-stu-id="a4c59-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

<span data-ttu-id="a4c59-119">Примечание. Вы можете использовать командлет **Wait-AzRecoveryServicesBackupJob** , чтобы дождаться завершения задания резервного копирования Azure вместо цикла while.</span><span class="sxs-lookup"><span data-stu-id="a4c59-119">Note: You can use **Wait-AzRecoveryServicesBackupJob** cmdlet to wait for an Azure Backup job to finish instead of While loop.</span></span>

## <span data-ttu-id="a4c59-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a4c59-120">PARAMETERS</span></span>

### <span data-ttu-id="a4c59-121">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="a4c59-121">-BackupManagementType</span></span>

<span data-ttu-id="a4c59-122">Указывает тип управления резервным копированием.</span><span class="sxs-lookup"><span data-stu-id="a4c59-122">Specifies the Backup management type.</span></span>
<span data-ttu-id="a4c59-123">В настоящее время поддерживается только AzureVM, AzureStorage.</span><span class="sxs-lookup"><span data-stu-id="a4c59-123">Currently, only AzureVM, AzureStorage is supported.</span></span>

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

### <span data-ttu-id="a4c59-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4c59-124">-DefaultProfile</span></span>

<span data-ttu-id="a4c59-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a4c59-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4c59-126">-From</span><span class="sxs-lookup"><span data-stu-id="a4c59-126">-From</span></span>

<span data-ttu-id="a4c59-127">Задает начало в качестве объекта **DateTime** для диапазона времени для задач, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a4c59-127">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="a4c59-128">Чтобы получить объект **DateTime** , используйте командлет **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="a4c59-128">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="a4c59-129">Чтобы получить дополнительные сведения о объектах **DateTime** , введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="a4c59-129">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="a4c59-130">Используйте формат UTC для дат.</span><span class="sxs-lookup"><span data-stu-id="a4c59-130">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="a4c59-131">-Job</span><span class="sxs-lookup"><span data-stu-id="a4c59-131">-Job</span></span>

<span data-ttu-id="a4c59-132">Указывает задание, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="a4c59-132">Specifies the job to get.</span></span>

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

### <span data-ttu-id="a4c59-133">-JobId</span><span class="sxs-lookup"><span data-stu-id="a4c59-133">-JobId</span></span>

<span data-ttu-id="a4c59-134">Указывает идентификатор задания, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a4c59-134">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="a4c59-135">Идентификатор — это свойство JobId объекта **Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. JobBase** .</span><span class="sxs-lookup"><span data-stu-id="a4c59-135">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

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

### <span data-ttu-id="a4c59-136">-Эксплуатация</span><span class="sxs-lookup"><span data-stu-id="a4c59-136">-Operation</span></span>

<span data-ttu-id="a4c59-137">Указывает операцию заданий, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a4c59-137">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="a4c59-138">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a4c59-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a4c59-139">Копирование</span><span class="sxs-lookup"><span data-stu-id="a4c59-139">Backup</span></span>
- <span data-ttu-id="a4c59-140">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="a4c59-140">ConfigureBackup</span></span>
- <span data-ttu-id="a4c59-141">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="a4c59-141">DeleteBackupData</span></span>
- <span data-ttu-id="a4c59-142">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="a4c59-142">DisableBackup</span></span>
- <span data-ttu-id="a4c59-143">Восстановление</span><span class="sxs-lookup"><span data-stu-id="a4c59-143">Restore</span></span>

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

### <span data-ttu-id="a4c59-144">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="a4c59-144">-Status</span></span>

<span data-ttu-id="a4c59-145">Указывает состояние заданий, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a4c59-145">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="a4c59-146">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a4c59-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a4c59-147">Ход выполнения</span><span class="sxs-lookup"><span data-stu-id="a4c59-147">InProgress</span></span>
- <span data-ttu-id="a4c59-148">Ошибкой</span><span class="sxs-lookup"><span data-stu-id="a4c59-148">Failed</span></span>
- <span data-ttu-id="a4c59-149">Отменен</span><span class="sxs-lookup"><span data-stu-id="a4c59-149">Cancelled</span></span>
- <span data-ttu-id="a4c59-150">Отмена</span><span class="sxs-lookup"><span data-stu-id="a4c59-150">Cancelling</span></span>
- <span data-ttu-id="a4c59-151">Completed</span><span class="sxs-lookup"><span data-stu-id="a4c59-151">Completed</span></span>
- <span data-ttu-id="a4c59-152">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="a4c59-152">CompletedWithWarnings</span></span>

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

### <span data-ttu-id="a4c59-153">-To</span><span class="sxs-lookup"><span data-stu-id="a4c59-153">-To</span></span>

<span data-ttu-id="a4c59-154">Задает конечный объект в качестве объекта **DateTime** из диапазона времени для задач, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a4c59-154">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="a4c59-155">Значение по умолчанию — текущее системное время.</span><span class="sxs-lookup"><span data-stu-id="a4c59-155">The default value is the current system time.</span></span>
<span data-ttu-id="a4c59-156">Если указать этот параметр, необходимо также указать параметр **-from** .</span><span class="sxs-lookup"><span data-stu-id="a4c59-156">If you specify this parameter, you must also specify the **-From** parameter.</span></span>
<span data-ttu-id="a4c59-157">Используйте формат UTC для дат.</span><span class="sxs-lookup"><span data-stu-id="a4c59-157">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="a4c59-158">-VaultId</span><span class="sxs-lookup"><span data-stu-id="a4c59-158">-VaultId</span></span>

<span data-ttu-id="a4c59-159">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="a4c59-159">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="a4c59-160">-CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4c59-160">-CommonParameters</span></span>

<span data-ttu-id="a4c59-161">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a4c59-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4c59-162">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4c59-162">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4c59-163">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a4c59-163">INPUTS</span></span>

### <span data-ttu-id="a4c59-164">System. String</span><span class="sxs-lookup"><span data-stu-id="a4c59-164">System.String</span></span>

## <span data-ttu-id="a4c59-165">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4c59-165">OUTPUTS</span></span>

### <span data-ttu-id="a4c59-166">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="a4c59-166">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="a4c59-167">Пуск</span><span class="sxs-lookup"><span data-stu-id="a4c59-167">NOTES</span></span>

## <span data-ttu-id="a4c59-168">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a4c59-168">RELATED LINKS</span></span>

[<span data-ttu-id="a4c59-169">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="a4c59-169">Get-AzRecoveryServicesBackupJobDetail</span></span>](./Get-AzRecoveryServicesBackupJobDetail.md)

[<span data-ttu-id="a4c59-170">Остановить-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="a4c59-170">Stop-AzRecoveryServicesBackupJob</span></span>](./Stop-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="a4c59-171">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="a4c59-171">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)
