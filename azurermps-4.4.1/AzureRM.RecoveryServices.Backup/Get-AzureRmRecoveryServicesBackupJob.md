---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: 3fb6b89f5708c951731c45e0d32e0f7a379cf754
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569263"
---
# <span data-ttu-id="9c8bb-101">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="9c8bb-101">Get-AzureRmRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="9c8bb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9c8bb-102">SYNOPSIS</span></span>
<span data-ttu-id="9c8bb-103">Получает задания резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="9c8bb-103">Gets Backup jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c8bb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9c8bb-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c8bb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c8bb-105">DESCRIPTION</span></span>
<span data-ttu-id="9c8bb-106">Командлет **Get-AzureRmRecoveryServicesBackupJob** получает задания резервного копирования Azure для определенного хранилища.</span><span class="sxs-lookup"><span data-stu-id="9c8bb-106">The **Get-AzureRmRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>

<span data-ttu-id="9c8bb-107">Настройте контекст хранилища с помощью командлета Set-AzureRmRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="9c8bb-107">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="9c8bb-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9c8bb-108">EXAMPLES</span></span>

### <span data-ttu-id="9c8bb-109">Пример 1: получение всех выполняемых заданий</span><span class="sxs-lookup"><span data-stu-id="9c8bb-109">Example 1: Get all in-progress jobs</span></span>
```
PS C:\>$Joblist = Get-AzureRMRecoveryservicesBackupJob -Status Inprogress
PS C:\> $Joblist[0]
WorkloadName     Operation            Status               StartTime                 EndTime                                             
------------     ---------            ------               ---------                 -------                                             
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="9c8bb-110">Первая команда получает состояние выполняющегося задания в виде массива, а затем сохраняет его в переменной $Joblist.</span><span class="sxs-lookup"><span data-stu-id="9c8bb-110">The first command gets status of an in-progress job as an array, and then stores it in the $Joblist variable.</span></span>

<span data-ttu-id="9c8bb-111">Вторая команда отображает первый элемент в массиве $Joblist.</span><span class="sxs-lookup"><span data-stu-id="9c8bb-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="9c8bb-112">Пример 2: получение всех невыполненных заданий за последние 7 дней</span><span class="sxs-lookup"><span data-stu-id="9c8bb-112">Example 2: Get all failed jobs in the last 7 days</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed
```

<span data-ttu-id="9c8bb-113">Эта команда возвращает задания с ошибкой за последнюю неделю в хранилище.</span><span class="sxs-lookup"><span data-stu-id="9c8bb-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="9c8bb-114">Параметр *from* указывает время, семь дней в прошлом, указанное в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="9c8bb-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="9c8bb-115">В команде не указывается значение параметра " *Кому* ".</span><span class="sxs-lookup"><span data-stu-id="9c8bb-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="9c8bb-116">Таким образом, используется значение по умолчанию для текущего времени.</span><span class="sxs-lookup"><span data-stu-id="9c8bb-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="9c8bb-117">Пример 3: получение выполняющегося задания и ожидание завершения</span><span class="sxs-lookup"><span data-stu-id="9c8bb-117">Example 3: Get an in-progress job and wait for completion</span></span>
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

<span data-ttu-id="9c8bb-118">Этот сценарий опрашивает первое задание, которое выполняется в данный момент, пока задание не будет завершено.</span><span class="sxs-lookup"><span data-stu-id="9c8bb-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="9c8bb-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9c8bb-119">PARAMETERS</span></span>

### <span data-ttu-id="9c8bb-120">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="9c8bb-120">-BackupManagementType</span></span>
<span data-ttu-id="9c8bb-121">Указывает тип управления резервным копированием.</span><span class="sxs-lookup"><span data-stu-id="9c8bb-121">Specifies the Backup management type.</span></span>
<span data-ttu-id="9c8bb-122">В настоящее время поддерживается только AzureVM.</span><span class="sxs-lookup"><span data-stu-id="9c8bb-122">Currently, only AzureVM is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c8bb-123">-From</span><span class="sxs-lookup"><span data-stu-id="9c8bb-123">-From</span></span>
<span data-ttu-id="9c8bb-124">Задает начало в качестве объекта **DateTime** для диапазона времени для задач, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9c8bb-124">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="9c8bb-125">Чтобы получить объект **DateTime** , используйте командлет Get-Date.</span><span class="sxs-lookup"><span data-stu-id="9c8bb-125">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="9c8bb-126">Чтобы получить дополнительные сведения о объектах **DateTime** , введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="9c8bb-126">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="9c8bb-127">Используйте формат UTC для дат.</span><span class="sxs-lookup"><span data-stu-id="9c8bb-127">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="9c8bb-128">-Job</span><span class="sxs-lookup"><span data-stu-id="9c8bb-128">-Job</span></span>
<span data-ttu-id="9c8bb-129">Указывает имя задания резервного копирования, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="9c8bb-129">Specifies the name of the Backup job to get.</span></span>

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

### <span data-ttu-id="9c8bb-130">-JobId</span><span class="sxs-lookup"><span data-stu-id="9c8bb-130">-JobId</span></span>
<span data-ttu-id="9c8bb-131">Указывает идентификатор задания, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9c8bb-131">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="9c8bb-132">Идентификатор — это свойство InstanceId объекта **AzureRmRecoveryServicesBackupJob** .</span><span class="sxs-lookup"><span data-stu-id="9c8bb-132">The ID is the InstanceId property of an **AzureRmRecoveryServicesBackupJob** object.</span></span>
<span data-ttu-id="9c8bb-133">Чтобы получить объект **AzureRmRecoveryServicesBackupJob** , используйте Get-AzureRmRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="9c8bb-133">To obtain an **AzureRmRecoveryServicesBackupJob** object, use Get-AzureRmRecoveryServicesBackupJob.</span></span>

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

### <span data-ttu-id="9c8bb-134">-Эксплуатация</span><span class="sxs-lookup"><span data-stu-id="9c8bb-134">-Operation</span></span>
<span data-ttu-id="9c8bb-135">Указывает операцию заданий, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9c8bb-135">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="9c8bb-136">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9c8bb-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9c8bb-137">Копирование</span><span class="sxs-lookup"><span data-stu-id="9c8bb-137">Backup</span></span>
- <span data-ttu-id="9c8bb-138">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="9c8bb-138">ConfigureBackup</span></span>
- <span data-ttu-id="9c8bb-139">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="9c8bb-139">DeleteBackupData</span></span>
- <span data-ttu-id="9c8bb-140">Отменить</span><span class="sxs-lookup"><span data-stu-id="9c8bb-140">Register</span></span>
- <span data-ttu-id="9c8bb-141">Восстановление</span><span class="sxs-lookup"><span data-stu-id="9c8bb-141">Restore</span></span>
- <span data-ttu-id="9c8bb-142">Снять защиту</span><span class="sxs-lookup"><span data-stu-id="9c8bb-142">UnProtect</span></span>
- <span data-ttu-id="9c8bb-143">Отмените регистрацию</span><span class="sxs-lookup"><span data-stu-id="9c8bb-143">Unregister</span></span>

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

### <span data-ttu-id="9c8bb-144">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="9c8bb-144">-Status</span></span>
<span data-ttu-id="9c8bb-145">Указывает состояние заданий, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9c8bb-145">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="9c8bb-146">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9c8bb-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9c8bb-147">Ход выполнения</span><span class="sxs-lookup"><span data-stu-id="9c8bb-147">InProgress</span></span>
- <span data-ttu-id="9c8bb-148">Ошибкой</span><span class="sxs-lookup"><span data-stu-id="9c8bb-148">Failed</span></span>
- <span data-ttu-id="9c8bb-149">Отменен</span><span class="sxs-lookup"><span data-stu-id="9c8bb-149">Cancelled</span></span>
- <span data-ttu-id="9c8bb-150">Отмена</span><span class="sxs-lookup"><span data-stu-id="9c8bb-150">Cancelling</span></span>
- <span data-ttu-id="9c8bb-151">Completed</span><span class="sxs-lookup"><span data-stu-id="9c8bb-151">Completed</span></span>
- <span data-ttu-id="9c8bb-152">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="9c8bb-152">CompletedWithWarnings</span></span>

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

### <span data-ttu-id="9c8bb-153">-To</span><span class="sxs-lookup"><span data-stu-id="9c8bb-153">-To</span></span>
<span data-ttu-id="9c8bb-154">Задает конечный объект в качестве объекта **DateTime** из диапазона времени для задач, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9c8bb-154">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="9c8bb-155">Значение по умолчанию — текущее системное время.</span><span class="sxs-lookup"><span data-stu-id="9c8bb-155">The default value is the current system time.</span></span>
<span data-ttu-id="9c8bb-156">Если указать этот параметр, необходимо также указать параметр *from* .</span><span class="sxs-lookup"><span data-stu-id="9c8bb-156">If you specify this parameter, you must also specify the *From* parameter.</span></span>
<span data-ttu-id="9c8bb-157">Используйте формат UTC для дат.</span><span class="sxs-lookup"><span data-stu-id="9c8bb-157">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="9c8bb-158">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c8bb-158">-DefaultProfile</span></span>
<span data-ttu-id="9c8bb-159">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9c8bb-159">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c8bb-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c8bb-160">CommonParameters</span></span>
<span data-ttu-id="9c8bb-161">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9c8bb-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c8bb-162">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c8bb-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c8bb-163">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9c8bb-163">INPUTS</span></span>

## <span data-ttu-id="9c8bb-164">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c8bb-164">OUTPUTS</span></span>

### <span data-ttu-id="9c8bb-165">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="9c8bb-165">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

### <span data-ttu-id="9c8bb-166">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. JobBase]</span><span class="sxs-lookup"><span data-stu-id="9c8bb-166">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase]</span></span>

## <span data-ttu-id="9c8bb-167">Пуск</span><span class="sxs-lookup"><span data-stu-id="9c8bb-167">NOTES</span></span>

## <span data-ttu-id="9c8bb-168">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9c8bb-168">RELATED LINKS</span></span>

[<span data-ttu-id="9c8bb-169">Get-AzureRmRecoveryServicesBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="9c8bb-169">Get-AzureRmRecoveryServicesBackupJobDetails</span></span>](./Get-AzureRmRecoveryServicesBackupJobDetails.md)

[<span data-ttu-id="9c8bb-170">Остановить-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="9c8bb-170">Stop-AzureRmRecoveryServicesBackupJob</span></span>](./Stop-AzureRmRecoveryServicesBackupJob.md)

[<span data-ttu-id="9c8bb-171">Wait-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="9c8bb-171">Wait-AzureRmRecoveryServicesBackupJob</span></span>](./Wait-AzureRmRecoveryServicesBackupJob.md)


