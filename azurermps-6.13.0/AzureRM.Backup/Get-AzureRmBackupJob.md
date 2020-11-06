---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 331F32CB-7777-401C-A42A-23098944CFBE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
ms.openlocfilehash: cbdb60fb4ec139b1dae92b7dd8e2e54675ae1f90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563135"
---
# <span data-ttu-id="020d6-101">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="020d6-101">Get-AzureRmBackupJob</span></span>

## <span data-ttu-id="020d6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="020d6-102">SYNOPSIS</span></span>
<span data-ttu-id="020d6-103">Получает задания резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="020d6-103">Gets Backup jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="020d6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="020d6-104">SYNTAX</span></span>

### <span data-ttu-id="020d6-105">"Фильтры" (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="020d6-105">FiltersSet (Default)</span></span>
```
Get-AzureRmBackupJob -Vault <AzureRMBackupVault> [-JobId <String>] [-From <DateTime>] [-To <DateTime>]
 [-Status <String>] [-Type <String>] [-Operation <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="020d6-106">JobsListFilter</span><span class="sxs-lookup"><span data-stu-id="020d6-106">JobsListFilter</span></span>
```
Get-AzureRmBackupJob -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="020d6-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="020d6-107">DESCRIPTION</span></span>
<span data-ttu-id="020d6-108">Командлет **Get-AzureRmBackupJob** получает задания резервного копирования Azure для определенного хранилища.</span><span class="sxs-lookup"><span data-stu-id="020d6-108">The **Get-AzureRmBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>

## <span data-ttu-id="020d6-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="020d6-109">EXAMPLES</span></span>

### <span data-ttu-id="020d6-110">Пример 1: получение всех заданий в резервном хранилище</span><span class="sxs-lookup"><span data-stu-id="020d6-110">Example 1: Get all jobs in a Backup vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupJob -Vault $Vault
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Backup          InProgress      26-Aug-15 12:24:01 PM  01-Jan-01 12:00:00 AM
co03-vm         ConfigureBackup Completed       26-Aug-15 12:19:49 PM  26-Aug-15 12:19:54 PM
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

<span data-ttu-id="020d6-111">Первая команда получает хранилище с именем Vault03 с помощью командлета **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="020d6-111">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="020d6-112">Команда сохраняет этот объект в переменной $Vault.</span><span class="sxs-lookup"><span data-stu-id="020d6-112">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="020d6-113">Вторая команда получает все задания для хранилища в $Vault.</span><span class="sxs-lookup"><span data-stu-id="020d6-113">The second command gets all the jobs for the vault in $Vault.</span></span>

### <span data-ttu-id="020d6-114">Пример 2: Получение завершенных заданий</span><span class="sxs-lookup"><span data-stu-id="020d6-114">Example 2: Get completed jobs</span></span>
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -Status Completed
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

<span data-ttu-id="020d6-115">Эта команда получает завершенные задания из хранилища в $Vault.</span><span class="sxs-lookup"><span data-stu-id="020d6-115">This command gets completed jobs from the vault in $Vault.</span></span>

### <span data-ttu-id="020d6-116">Пример 3: получение заданий со сбоем за последнюю неделю</span><span class="sxs-lookup"><span data-stu-id="020d6-116">Example 3: Get failed jobs for the last week</span></span>
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -From (Get-Date).AddDays(-7) -Status Failed
```

<span data-ttu-id="020d6-117">Эта команда возвращает задания с ошибкой за последнюю неделю из хранилища в $Vault.</span><span class="sxs-lookup"><span data-stu-id="020d6-117">This command gets failed jobs from the last week from the vault in $Vault.</span></span>
<span data-ttu-id="020d6-118">Параметр *from* указывает время в прошлом на семь дней.</span><span class="sxs-lookup"><span data-stu-id="020d6-118">The *From* parameter specifies a time seven days in the past.</span></span>
<span data-ttu-id="020d6-119">В команде не указывается значение параметра " *Кому* ".</span><span class="sxs-lookup"><span data-stu-id="020d6-119">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="020d6-120">Таким образом, используется значение по умолчанию для текущего времени.</span><span class="sxs-lookup"><span data-stu-id="020d6-120">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="020d6-121">Пример 4: создание резервной копии для выполняемого задания, которое завершается</span><span class="sxs-lookup"><span data-stu-id="020d6-121">Example 4: Poll Backup for an in progress job that finishes</span></span>
```
PS C:\>$Jobs = Get-AzureRmBackupJob -Vault $Vault -Status InProgress
$Job = $Jobs[0] 
while ( $Job.Status -ne Completed ) 
{
   Write-Host "Waiting for completion..." 
   Start-Sleep -Seconds 10
   $job = Get-AzureRmBackupJob -Vault $Vault -Job $Job
}
Write-Host "Done!"
Waiting for completion... 
Waiting for completion... 
Waiting for completion... 
Done!
```

<span data-ttu-id="020d6-122">Этот сценарий опрашивает первое задание, которое выполняется в данный момент, пока задание не будет завершено.</span><span class="sxs-lookup"><span data-stu-id="020d6-122">This script polls the first job that is currently in progress until the job has completed.</span></span>
<span data-ttu-id="020d6-123">В первой строке сценария возвращаются все задания в $Vault, которые находятся в процессе выполнения, а затем эти задания сохраняются в переменной массива $Jobs.</span><span class="sxs-lookup"><span data-stu-id="020d6-123">The first line of the script gets all the jobs in $Vault that are in progress, and then stores those jobs in the $Jobs array variable.</span></span>
<span data-ttu-id="020d6-124">Вторая строка сохраняет первое задание из массива $Jobs в переменной $Job.</span><span class="sxs-lookup"><span data-stu-id="020d6-124">The second line stores the first job from the $Jobs array in the $Job variable.</span></span>
<span data-ttu-id="020d6-125">Третья строка начинается с цикла **while** , который проверяет текущее состояние задания до завершения задания.</span><span class="sxs-lookup"><span data-stu-id="020d6-125">The third line starts a **while** loop that checks the current status of the job until the job is completed.</span></span>
<span data-ttu-id="020d6-126">Чтобы получить сведения о ключевом слове " **время** ", введите `Get-Help about_While` .</span><span class="sxs-lookup"><span data-stu-id="020d6-126">For information about the **while** keyword, type `Get-Help about_While`.</span></span>
<span data-ttu-id="020d6-127">Цикл **while** записывает на консоль сообщение, заждет десять секунд, а затем обновляет переменную $Job.</span><span class="sxs-lookup"><span data-stu-id="020d6-127">The **while** loop writes a message to the console, sleeps for ten seconds, and then updates the $Job variable.</span></span>
<span data-ttu-id="020d6-128">Сценарий обновляет переменную $Job с помощью существующего значения $Job и текущего командлета, чтобы получить текущее состояние задания.</span><span class="sxs-lookup"><span data-stu-id="020d6-128">The script updates the $Job variable by using existing value of $Job and the current cmdlet to get the current status of the job.</span></span>
<span data-ttu-id="020d6-129">Чтобы получить сведения о командлетах Windows PowerShell, введите `Get-Help Write-Host` и `Get-Help Start-Sleep` .</span><span class="sxs-lookup"><span data-stu-id="020d6-129">For information about the Windows PowerShell cmdlets, type `Get-Help Write-Host` and `Get-Help Start-Sleep`.</span></span>
<span data-ttu-id="020d6-130">В последней строке сценария сообщается, что сценарий завершен.</span><span class="sxs-lookup"><span data-stu-id="020d6-130">The final line of the script tells you that the script has finished.</span></span>

## <span data-ttu-id="020d6-131">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="020d6-131">PARAMETERS</span></span>

### <span data-ttu-id="020d6-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="020d6-132">-DefaultProfile</span></span>
<span data-ttu-id="020d6-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="020d6-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="020d6-134">-From</span><span class="sxs-lookup"><span data-stu-id="020d6-134">-From</span></span>
<span data-ttu-id="020d6-135">Задает начало в качестве объекта **DateTime** для диапазона времени для задач, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="020d6-135">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="020d6-136">Чтобы получить объект **DateTime** , используйте командлет Get-Date.</span><span class="sxs-lookup"><span data-stu-id="020d6-136">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="020d6-137">Чтобы получить дополнительные сведения о объектах **DateTime** , введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="020d6-137">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: FiltersSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="020d6-138">-Job</span><span class="sxs-lookup"><span data-stu-id="020d6-138">-Job</span></span>
<span data-ttu-id="020d6-139">Указывает задание, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="020d6-139">Specifies a job that this cmdlet gets.</span></span>
<span data-ttu-id="020d6-140">Чтобы получить объект **AzureRmBackupJob** , используйте командлет Get-AzureRmBackupJob.</span><span class="sxs-lookup"><span data-stu-id="020d6-140">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob
Parameter Sets: JobsListFilter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="020d6-141">-JobId</span><span class="sxs-lookup"><span data-stu-id="020d6-141">-JobId</span></span>
<span data-ttu-id="020d6-142">Указывает идентификатор задания, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="020d6-142">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="020d6-143">Идентификатор — это свойство **InstanceId** объекта **AzureRmBackupJob** .</span><span class="sxs-lookup"><span data-stu-id="020d6-143">The ID is the **InstanceId** property of an **AzureRmBackupJob** object.</span></span>
<span data-ttu-id="020d6-144">Чтобы получить объект **AzureRmBackupJob** , используйте Get-AzureRmBackupJob.</span><span class="sxs-lookup"><span data-stu-id="020d6-144">To obtain an **AzureRmBackupJob** object, use Get-AzureRmBackupJob.</span></span>

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="020d6-145">-Эксплуатация</span><span class="sxs-lookup"><span data-stu-id="020d6-145">-Operation</span></span>
<span data-ttu-id="020d6-146">Указывает операцию заданий, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="020d6-146">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="020d6-147">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="020d6-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="020d6-148">Копирование</span><span class="sxs-lookup"><span data-stu-id="020d6-148">Backup</span></span> 
- <span data-ttu-id="020d6-149">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="020d6-149">ConfigureBackup</span></span> 
- <span data-ttu-id="020d6-150">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="020d6-150">DeleteBackupData</span></span> 
- <span data-ttu-id="020d6-151">Отменить</span><span class="sxs-lookup"><span data-stu-id="020d6-151">Register</span></span> 
- <span data-ttu-id="020d6-152">Восстановление</span><span class="sxs-lookup"><span data-stu-id="020d6-152">Restore</span></span> 
- <span data-ttu-id="020d6-153">Снять защиту</span><span class="sxs-lookup"><span data-stu-id="020d6-153">UnProtect</span></span> 
- <span data-ttu-id="020d6-154">Отмените регистрацию</span><span class="sxs-lookup"><span data-stu-id="020d6-154">Unregister</span></span>

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases:
Accepted values: Backup, ConfigureBackup, DeleteBackupData, Register, Restore, UnProtect, Unregister

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="020d6-155">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="020d6-155">-Status</span></span>
<span data-ttu-id="020d6-156">Указывает состояние заданий, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="020d6-156">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="020d6-157">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="020d6-157">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="020d6-158">Ход выполнения</span><span class="sxs-lookup"><span data-stu-id="020d6-158">InProgress</span></span>
- <span data-ttu-id="020d6-159">Ошибкой</span><span class="sxs-lookup"><span data-stu-id="020d6-159">Failed</span></span>
- <span data-ttu-id="020d6-160">Отменен</span><span class="sxs-lookup"><span data-stu-id="020d6-160">Cancelled</span></span>
- <span data-ttu-id="020d6-161">Отмена</span><span class="sxs-lookup"><span data-stu-id="020d6-161">Cancelling</span></span>
- <span data-ttu-id="020d6-162">Completed</span><span class="sxs-lookup"><span data-stu-id="020d6-162">Completed</span></span>
- <span data-ttu-id="020d6-163">CompletedWithWarnings. можно указать этот параметр, чтобы найти все выполняемые задания или все задания, завершившихся сбоем.</span><span class="sxs-lookup"><span data-stu-id="020d6-163">CompletedWithWarnings You can specify this parameter to find all in progress jobs or all failed jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases:
Accepted values: Cancelled, Cancelling, Completed, CompletedWithWarnings, Failed, InProgress

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="020d6-164">-To</span><span class="sxs-lookup"><span data-stu-id="020d6-164">-To</span></span>
<span data-ttu-id="020d6-165">Задает конечный объект в качестве объекта **DateTime** из диапазона времени для задач, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="020d6-165">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="020d6-166">Значение по умолчанию — текущее системное время.</span><span class="sxs-lookup"><span data-stu-id="020d6-166">The default value is the current system time.</span></span>
<span data-ttu-id="020d6-167">Если указать этот параметр, необходимо также указать параметр *from* .</span><span class="sxs-lookup"><span data-stu-id="020d6-167">If you specify this parameter, you must also specify the *From* parameter.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: FiltersSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="020d6-168">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="020d6-168">-Type</span></span>
<span data-ttu-id="020d6-169">Указывает тип контейнера, для которого этот командлет получает задания резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="020d6-169">Specifies the type of container for which this cmdlet gets backup jobs.</span></span>
<span data-ttu-id="020d6-170">В настоящее время единственным поддерживаемым значением является значение AzureVM.</span><span class="sxs-lookup"><span data-stu-id="020d6-170">Currently, the only supported value is AzureVM.</span></span>

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases:
Accepted values: AzureVM

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="020d6-171">-Хранилище</span><span class="sxs-lookup"><span data-stu-id="020d6-171">-Vault</span></span>
<span data-ttu-id="020d6-172">Указывает хранилище резервных копий, для которого этот командлет получает задания.</span><span class="sxs-lookup"><span data-stu-id="020d6-172">Specifies the Backup vault for which this cmdlet gets jobs.</span></span>
<span data-ttu-id="020d6-173">Чтобы получить объект **AzureRmBackupVault** , используйте командлет Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="020d6-173">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: FiltersSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="020d6-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="020d6-174">CommonParameters</span></span>
<span data-ttu-id="020d6-175">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="020d6-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="020d6-176">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="020d6-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="020d6-177">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="020d6-177">INPUTS</span></span>

### <span data-ttu-id="020d6-178">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="020d6-178">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault</span></span>
<span data-ttu-id="020d6-179">Параметры: хранилище (ByValue)</span><span class="sxs-lookup"><span data-stu-id="020d6-179">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="020d6-180">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="020d6-180">OUTPUTS</span></span>

### <span data-ttu-id="020d6-181">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupJob</span><span class="sxs-lookup"><span data-stu-id="020d6-181">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>

## <span data-ttu-id="020d6-182">Пуск</span><span class="sxs-lookup"><span data-stu-id="020d6-182">NOTES</span></span>
* <span data-ttu-id="020d6-183">Ничего</span><span class="sxs-lookup"><span data-stu-id="020d6-183">None</span></span>

## <span data-ttu-id="020d6-184">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="020d6-184">RELATED LINKS</span></span>

[<span data-ttu-id="020d6-185">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="020d6-185">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="020d6-186">Остановить-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="020d6-186">Stop-AzureRmBackupJob</span></span>](./Stop-AzureRmBackupJob.md)

[<span data-ttu-id="020d6-187">Wait-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="020d6-187">Wait-AzureRmBackupJob</span></span>](./Wait-AzureRmBackupJob.md)


