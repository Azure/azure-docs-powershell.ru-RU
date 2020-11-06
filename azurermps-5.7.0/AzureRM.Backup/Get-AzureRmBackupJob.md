---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 331F32CB-7777-401C-A42A-23098944CFBE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
ms.openlocfilehash: 3402dc7018f094a5f95a967385d9bae8d70c68f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561924"
---
# <span data-ttu-id="a6d6d-101">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="a6d6d-101">Get-AzureRmBackupJob</span></span>

## <span data-ttu-id="a6d6d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a6d6d-102">SYNOPSIS</span></span>
<span data-ttu-id="a6d6d-103">Получает задания резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="a6d6d-103">Gets Backup jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6d6d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a6d6d-104">SYNTAX</span></span>

### <span data-ttu-id="a6d6d-105">"Фильтры" (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a6d6d-105">FiltersSet (Default)</span></span>
```
Get-AzureRmBackupJob -Vault <AzureRMBackupVault> [-JobId <String>] [-From <DateTime>] [-To <DateTime>]
 [-Status <String>] [-Type <String>] [-Operation <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a6d6d-106">JobsListFilter</span><span class="sxs-lookup"><span data-stu-id="a6d6d-106">JobsListFilter</span></span>
```
Get-AzureRmBackupJob -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6d6d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6d6d-107">DESCRIPTION</span></span>
<span data-ttu-id="a6d6d-108">Командлет **Get-AzureRmBackupJob** получает задания резервного копирования Azure для определенного хранилища.</span><span class="sxs-lookup"><span data-stu-id="a6d6d-108">The **Get-AzureRmBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>

## <span data-ttu-id="a6d6d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a6d6d-109">EXAMPLES</span></span>

### <span data-ttu-id="a6d6d-110">Пример 1: получение всех заданий в резервном хранилище</span><span class="sxs-lookup"><span data-stu-id="a6d6d-110">Example 1: Get all jobs in a Backup vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupJob -Vault $Vault
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Backup          InProgress      26-Aug-15 12:24:01 PM  01-Jan-01 12:00:00 AM
co03-vm         ConfigureBackup Completed       26-Aug-15 12:19:49 PM  26-Aug-15 12:19:54 PM
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

<span data-ttu-id="a6d6d-111">Первая команда получает хранилище с именем Vault03 с помощью командлета **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="a6d6d-111">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="a6d6d-112">Команда сохраняет этот объект в переменной $Vault.</span><span class="sxs-lookup"><span data-stu-id="a6d6d-112">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="a6d6d-113">Вторая команда получает все задания для хранилища в $Vault.</span><span class="sxs-lookup"><span data-stu-id="a6d6d-113">The second command gets all the jobs for the vault in $Vault.</span></span>

### <span data-ttu-id="a6d6d-114">Пример 2: Получение завершенных заданий</span><span class="sxs-lookup"><span data-stu-id="a6d6d-114">Example 2: Get completed jobs</span></span>
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -Status Completed
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

<span data-ttu-id="a6d6d-115">Эта команда получает завершенные задания из хранилища в $Vault.</span><span class="sxs-lookup"><span data-stu-id="a6d6d-115">This command gets completed jobs from the vault in $Vault.</span></span>

### <span data-ttu-id="a6d6d-116">Пример 3: получение заданий со сбоем за последнюю неделю</span><span class="sxs-lookup"><span data-stu-id="a6d6d-116">Example 3: Get failed jobs for the last week</span></span>
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -From (Get-Date).AddDays(-7) -Status Failed
```

<span data-ttu-id="a6d6d-117">Эта команда возвращает задания с ошибкой за последнюю неделю из хранилища в $Vault.</span><span class="sxs-lookup"><span data-stu-id="a6d6d-117">This command gets failed jobs from the last week from the vault in $Vault.</span></span>
<span data-ttu-id="a6d6d-118">Параметр *from* указывает время в прошлом на семь дней.</span><span class="sxs-lookup"><span data-stu-id="a6d6d-118">The *From* parameter specifies a time seven days in the past.</span></span>
<span data-ttu-id="a6d6d-119">В команде не указывается значение параметра " *Кому* ".</span><span class="sxs-lookup"><span data-stu-id="a6d6d-119">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="a6d6d-120">Таким образом, используется значение по умолчанию для текущего времени.</span><span class="sxs-lookup"><span data-stu-id="a6d6d-120">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="a6d6d-121">Пример 4: создание резервной копии для выполняемого задания, которое завершается</span><span class="sxs-lookup"><span data-stu-id="a6d6d-121">Example 4: Poll Backup for an in progress job that finishes</span></span>
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

<span data-ttu-id="a6d6d-122">Этот сценарий опрашивает первое задание, которое выполняется в данный момент, пока задание не будет завершено.</span><span class="sxs-lookup"><span data-stu-id="a6d6d-122">This script polls the first job that is currently in progress until the job has completed.</span></span>

<span data-ttu-id="a6d6d-123">В первой строке сценария возвращаются все задания в $Vault, которые находятся в процессе выполнения, а затем эти задания сохраняются в переменной массива $Jobs.</span><span class="sxs-lookup"><span data-stu-id="a6d6d-123">The first line of the script gets all the jobs in $Vault that are in progress, and then stores those jobs in the $Jobs array variable.</span></span>

<span data-ttu-id="a6d6d-124">Вторая строка сохраняет первое задание из массива $Jobs в переменной $Job.</span><span class="sxs-lookup"><span data-stu-id="a6d6d-124">The second line stores the first job from the $Jobs array in the $Job variable.</span></span>

<span data-ttu-id="a6d6d-125">Третья строка начинается с цикла **while** , который проверяет текущее состояние задания до завершения задания.</span><span class="sxs-lookup"><span data-stu-id="a6d6d-125">The third line starts a **while** loop that checks the current status of the job until the job is completed.</span></span>
<span data-ttu-id="a6d6d-126">Чтобы получить сведения о ключевом слове " **время** ", введите `Get-Help about_While` .</span><span class="sxs-lookup"><span data-stu-id="a6d6d-126">For information about the **while** keyword, type `Get-Help about_While`.</span></span>

<span data-ttu-id="a6d6d-127">Цикл **while** записывает на консоль сообщение, заждет десять секунд, а затем обновляет переменную $Job.</span><span class="sxs-lookup"><span data-stu-id="a6d6d-127">The **while** loop writes a message to the console, sleeps for ten seconds, and then updates the $Job variable.</span></span>
<span data-ttu-id="a6d6d-128">Сценарий обновляет переменную $Job с помощью существующего значения $Job и текущего командлета, чтобы получить текущее состояние задания.</span><span class="sxs-lookup"><span data-stu-id="a6d6d-128">The script updates the $Job variable by using existing value of $Job and the current cmdlet to get the current status of the job.</span></span>
<span data-ttu-id="a6d6d-129">Чтобы получить сведения о командлетах Windows PowerShell, введите `Get-Help Write-Host` и `Get-Help Start-Sleep` .</span><span class="sxs-lookup"><span data-stu-id="a6d6d-129">For information about the Windows PowerShell cmdlets, type `Get-Help Write-Host` and `Get-Help Start-Sleep`.</span></span>

<span data-ttu-id="a6d6d-130">В последней строке сценария сообщается, что сценарий завершен.</span><span class="sxs-lookup"><span data-stu-id="a6d6d-130">The final line of the script tells you that the script has finished.</span></span>

## <span data-ttu-id="a6d6d-131">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a6d6d-131">PARAMETERS</span></span>

### <span data-ttu-id="a6d6d-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6d6d-132">-DefaultProfile</span></span>
<span data-ttu-id="a6d6d-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a6d6d-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6d6d-134">-From</span><span class="sxs-lookup"><span data-stu-id="a6d6d-134">-From</span></span>
<span data-ttu-id="a6d6d-135">Задает начало в качестве объекта **DateTime** для диапазона времени для задач, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a6d6d-135">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="a6d6d-136">Чтобы получить объект **DateTime** , используйте командлет Get-Date.</span><span class="sxs-lookup"><span data-stu-id="a6d6d-136">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="a6d6d-137">Чтобы получить дополнительные сведения о объектах **DateTime** , введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="a6d6d-137">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6d6d-138">-Job</span><span class="sxs-lookup"><span data-stu-id="a6d6d-138">-Job</span></span>
<span data-ttu-id="a6d6d-139">Указывает задание, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a6d6d-139">Specifies a job that this cmdlet gets.</span></span>
<span data-ttu-id="a6d6d-140">Чтобы получить объект **AzureRmBackupJob** , используйте командлет Get-AzureRmBackupJob.</span><span class="sxs-lookup"><span data-stu-id="a6d6d-140">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: AzureRMBackupJob
Parameter Sets: JobsListFilter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6d6d-141">-JobId</span><span class="sxs-lookup"><span data-stu-id="a6d6d-141">-JobId</span></span>
<span data-ttu-id="a6d6d-142">Указывает идентификатор задания, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a6d6d-142">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="a6d6d-143">Идентификатор — это свойство **InstanceId** объекта **AzureRmBackupJob** .</span><span class="sxs-lookup"><span data-stu-id="a6d6d-143">The ID is the **InstanceId** property of an **AzureRmBackupJob** object.</span></span>
<span data-ttu-id="a6d6d-144">Чтобы получить объект **AzureRmBackupJob** , используйте Get-AzureRmBackupJob.</span><span class="sxs-lookup"><span data-stu-id="a6d6d-144">To obtain an **AzureRmBackupJob** object, use Get-AzureRmBackupJob.</span></span>

```yaml
Type: String
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6d6d-145">-Эксплуатация</span><span class="sxs-lookup"><span data-stu-id="a6d6d-145">-Operation</span></span>
<span data-ttu-id="a6d6d-146">Указывает операцию заданий, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a6d6d-146">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="a6d6d-147">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a6d6d-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a6d6d-148">Копирование</span><span class="sxs-lookup"><span data-stu-id="a6d6d-148">Backup</span></span> 
- <span data-ttu-id="a6d6d-149">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="a6d6d-149">ConfigureBackup</span></span> 
- <span data-ttu-id="a6d6d-150">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="a6d6d-150">DeleteBackupData</span></span> 
- <span data-ttu-id="a6d6d-151">Отменить</span><span class="sxs-lookup"><span data-stu-id="a6d6d-151">Register</span></span> 
- <span data-ttu-id="a6d6d-152">Восстановление</span><span class="sxs-lookup"><span data-stu-id="a6d6d-152">Restore</span></span> 
- <span data-ttu-id="a6d6d-153">Снять защиту</span><span class="sxs-lookup"><span data-stu-id="a6d6d-153">UnProtect</span></span> 
- <span data-ttu-id="a6d6d-154">Отмените регистрацию</span><span class="sxs-lookup"><span data-stu-id="a6d6d-154">Unregister</span></span>

```yaml
Type: String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: Backup, ConfigureBackup, DeleteBackupData, Register, Restore, UnProtect, Unregister

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6d6d-155">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="a6d6d-155">-Status</span></span>
<span data-ttu-id="a6d6d-156">Указывает состояние заданий, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a6d6d-156">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="a6d6d-157">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a6d6d-157">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a6d6d-158">Ход выполнения</span><span class="sxs-lookup"><span data-stu-id="a6d6d-158">InProgress</span></span>
- <span data-ttu-id="a6d6d-159">Ошибкой</span><span class="sxs-lookup"><span data-stu-id="a6d6d-159">Failed</span></span>
- <span data-ttu-id="a6d6d-160">Отменен</span><span class="sxs-lookup"><span data-stu-id="a6d6d-160">Cancelled</span></span>
- <span data-ttu-id="a6d6d-161">Отмена</span><span class="sxs-lookup"><span data-stu-id="a6d6d-161">Cancelling</span></span>
- <span data-ttu-id="a6d6d-162">Completed</span><span class="sxs-lookup"><span data-stu-id="a6d6d-162">Completed</span></span>
- <span data-ttu-id="a6d6d-163">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="a6d6d-163">CompletedWithWarnings</span></span> 

<span data-ttu-id="a6d6d-164">Вы можете указать этот параметр, чтобы найти все выполняемые задания или все задания, для которых произошел сбой.</span><span class="sxs-lookup"><span data-stu-id="a6d6d-164">You can specify this parameter to find all in progress jobs or all failed jobs.</span></span>

```yaml
Type: String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: Cancelled, Cancelling, Completed, CompletedWithWarnings, Failed, InProgress

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6d6d-165">-To</span><span class="sxs-lookup"><span data-stu-id="a6d6d-165">-To</span></span>
<span data-ttu-id="a6d6d-166">Задает конечный объект в качестве объекта **DateTime** из диапазона времени для задач, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a6d6d-166">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="a6d6d-167">Значение по умолчанию — текущее системное время.</span><span class="sxs-lookup"><span data-stu-id="a6d6d-167">The default value is the current system time.</span></span>
<span data-ttu-id="a6d6d-168">Если указать этот параметр, необходимо также указать параметр *from* .</span><span class="sxs-lookup"><span data-stu-id="a6d6d-168">If you specify this parameter, you must also specify the *From* parameter.</span></span>

```yaml
Type: DateTime
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6d6d-169">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="a6d6d-169">-Type</span></span>
<span data-ttu-id="a6d6d-170">Указывает тип контейнера, для которого этот командлет получает задания резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="a6d6d-170">Specifies the type of container for which this cmdlet gets backup jobs.</span></span>
<span data-ttu-id="a6d6d-171">В настоящее время единственным поддерживаемым значением является значение AzureVM.</span><span class="sxs-lookup"><span data-stu-id="a6d6d-171">Currently, the only supported value is AzureVM.</span></span>

```yaml
Type: String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: AzureVM

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6d6d-172">-Хранилище</span><span class="sxs-lookup"><span data-stu-id="a6d6d-172">-Vault</span></span>
<span data-ttu-id="a6d6d-173">Указывает хранилище резервных копий, для которого этот командлет получает задания.</span><span class="sxs-lookup"><span data-stu-id="a6d6d-173">Specifies the Backup vault for which this cmdlet gets jobs.</span></span>
<span data-ttu-id="a6d6d-174">Чтобы получить объект **AzureRmBackupVault** , используйте командлет Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="a6d6d-174">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: AzureRMBackupVault
Parameter Sets: FiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6d6d-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6d6d-175">CommonParameters</span></span>
<span data-ttu-id="a6d6d-176">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a6d6d-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6d6d-177">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6d6d-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6d6d-178">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a6d6d-178">INPUTS</span></span>

### <span data-ttu-id="a6d6d-179">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="a6d6d-179">AzureRmBackupVault</span></span>

## <span data-ttu-id="a6d6d-180">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6d6d-180">OUTPUTS</span></span>

### <span data-ttu-id="a6d6d-181">AzureRmBackupJob[]</span><span class="sxs-lookup"><span data-stu-id="a6d6d-181">AzureRmBackupJob[]</span></span>
<span data-ttu-id="a6d6d-182">Этот командлет возвращает одно или несколько заданий резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="a6d6d-182">This cmdlet returns one or more Backup jobs.</span></span>

## <span data-ttu-id="a6d6d-183">Пуск</span><span class="sxs-lookup"><span data-stu-id="a6d6d-183">NOTES</span></span>
* <span data-ttu-id="a6d6d-184">Ничего</span><span class="sxs-lookup"><span data-stu-id="a6d6d-184">None</span></span>

## <span data-ttu-id="a6d6d-185">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a6d6d-185">RELATED LINKS</span></span>

[<span data-ttu-id="a6d6d-186">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="a6d6d-186">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="a6d6d-187">Остановить-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="a6d6d-187">Stop-AzureRmBackupJob</span></span>](./Stop-AzureRmBackupJob.md)

[<span data-ttu-id="a6d6d-188">Wait-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="a6d6d-188">Wait-AzureRmBackupJob</span></span>](./Wait-AzureRmBackupJob.md)


