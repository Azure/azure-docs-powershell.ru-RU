---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A0293D80-5935-4D2C-AF11-2837FEC95760
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: ca480d266f4ab7706841fb901fa714dbe632ec2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557368"
---
# <span data-ttu-id="c010a-101">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c010a-101">Get-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="c010a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c010a-102">SYNOPSIS</span></span>
<span data-ttu-id="c010a-103">Получает задание Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="c010a-103">Gets a Data Lake Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c010a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c010a-104">SYNTAX</span></span>

### <span data-ttu-id="c010a-105">GetAllInResourceGroupAndAccount (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c010a-105">GetAllInResourceGroupAndAccount (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [[-Name] <String>] [[-Submitter] <String>]
 [[-SubmittedAfter] <DateTimeOffset>] [[-SubmittedBefore] <DateTimeOffset>] [[-State] <JobState[]>]
 [[-Result] <JobResult[]>] [-Top <Int32>] [-PipelineId <Guid>] [-RecurrenceId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c010a-106">GetBySpecificJobInformation</span><span class="sxs-lookup"><span data-stu-id="c010a-106">GetBySpecificJobInformation</span></span>
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-Include] <ExtendedJobData>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c010a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c010a-107">DESCRIPTION</span></span>
<span data-ttu-id="c010a-108">Командлет **Get-AzureRmDataLakeAnalyticsJob** получает задание Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="c010a-108">The **Get-AzureRmDataLakeAnalyticsJob** cmdlet gets an Azure Data Lake Analytics job.</span></span>
<span data-ttu-id="c010a-109">Если задание не задано, этот командлет получает все задания.</span><span class="sxs-lookup"><span data-stu-id="c010a-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="c010a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c010a-110">EXAMPLES</span></span>

### <span data-ttu-id="c010a-111">Пример 1: получение указанного задания</span><span class="sxs-lookup"><span data-stu-id="c010a-111">Example 1: Get a specified job</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -JobId $JobID01
```

<span data-ttu-id="c010a-112">Эта команда получает задание с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="c010a-112">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="c010a-113">Пример 2: получение заданий, отправленных за последнюю неделю</span><span class="sxs-lookup"><span data-stu-id="c010a-113">Example 2: Get jobs submitted in the past week</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -SubmittedAfter (Get-Date).AddDays(-7)
```

<span data-ttu-id="c010a-114">Эта команда получает задания, отправленные за последнюю неделю.</span><span class="sxs-lookup"><span data-stu-id="c010a-114">This command gets jobs submitted in the past week.</span></span>

## <span data-ttu-id="c010a-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c010a-115">PARAMETERS</span></span>

### <span data-ttu-id="c010a-116">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="c010a-116">-Account</span></span>
<span data-ttu-id="c010a-117">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="c010a-117">Specifies the name of a Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c010a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c010a-118">-DefaultProfile</span></span>
<span data-ttu-id="c010a-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c010a-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c010a-120">-Include</span><span class="sxs-lookup"><span data-stu-id="c010a-120">-Include</span></span>
<span data-ttu-id="c010a-121">Задает параметры, указывающие тип дополнительной информации, которую требуется получить о задании.</span><span class="sxs-lookup"><span data-stu-id="c010a-121">Specifies options that indicate the type of additional information to retrieve about the job.</span></span>
<span data-ttu-id="c010a-122">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c010a-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c010a-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="c010a-123">None</span></span>
- <span data-ttu-id="c010a-124">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="c010a-124">DebugInfo</span></span>
- <span data-ttu-id="c010a-125">Сведения</span><span class="sxs-lookup"><span data-stu-id="c010a-125">Statistics</span></span>
- <span data-ttu-id="c010a-126">Весь</span><span class="sxs-lookup"><span data-stu-id="c010a-126">All</span></span>

```yaml
Type: ExtendedJobData
Parameter Sets: GetBySpecificJobInformation
Aliases: 
Accepted values: None, All, DebugInfo, Statistics

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c010a-127">-JobId</span><span class="sxs-lookup"><span data-stu-id="c010a-127">-JobId</span></span>
<span data-ttu-id="c010a-128">Указывает ИД задания, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="c010a-128">Specifies the ID of the job to get.</span></span>

```yaml
Type: Guid
Parameter Sets: GetBySpecificJobInformation
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c010a-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c010a-129">-Name</span></span>
<span data-ttu-id="c010a-130">Указывает имя, которое будет использоваться для фильтрации результатов списка заданий.</span><span class="sxs-lookup"><span data-stu-id="c010a-130">Specifies a name to use to filter the job list results.</span></span>
<span data-ttu-id="c010a-131">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c010a-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c010a-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="c010a-132">None</span></span>
- <span data-ttu-id="c010a-133">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="c010a-133">DebugInfo</span></span>
- <span data-ttu-id="c010a-134">Сведения</span><span class="sxs-lookup"><span data-stu-id="c010a-134">Statistics</span></span>
- <span data-ttu-id="c010a-135">Весь</span><span class="sxs-lookup"><span data-stu-id="c010a-135">All</span></span>

```yaml
Type: String
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c010a-136">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="c010a-136">-PipelineId</span></span>
<span data-ttu-id="c010a-137">Необязательный идентификатор, указывающий на то, что должны возвращаться только задания, входящие в указанный конвейер.</span><span class="sxs-lookup"><span data-stu-id="c010a-137">An optional ID that indicates only jobs part of the specified pipeline should be returned.</span></span>

```yaml
Type: Guid
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c010a-138">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="c010a-138">-RecurrenceId</span></span>
<span data-ttu-id="c010a-139">Необязательный идентификатор, указывающий на то, что должны возвращаться только задания, входящие в указанное повторение.</span><span class="sxs-lookup"><span data-stu-id="c010a-139">An optional ID that indicates only jobs part of the specified recurrence should be returned.</span></span>

```yaml
Type: Guid
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c010a-140">-Result (результат)</span><span class="sxs-lookup"><span data-stu-id="c010a-140">-Result</span></span>
<span data-ttu-id="c010a-141">Указывает фильтр результатов для результатов задания.</span><span class="sxs-lookup"><span data-stu-id="c010a-141">Specifies a result filter for the job results.</span></span>
<span data-ttu-id="c010a-142">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c010a-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c010a-143">Ничего</span><span class="sxs-lookup"><span data-stu-id="c010a-143">None</span></span>
- <span data-ttu-id="c010a-144">Отменен</span><span class="sxs-lookup"><span data-stu-id="c010a-144">Cancelled</span></span>
- <span data-ttu-id="c010a-145">Ошибкой</span><span class="sxs-lookup"><span data-stu-id="c010a-145">Failed</span></span>
- <span data-ttu-id="c010a-146">LSP</span><span class="sxs-lookup"><span data-stu-id="c010a-146">Succeeded</span></span>

```yaml
Type: JobResult[]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 
Accepted values: None, Succeeded, Cancelled, Failed

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c010a-147">-State</span><span class="sxs-lookup"><span data-stu-id="c010a-147">-State</span></span>
<span data-ttu-id="c010a-148">Указывает фильтр состояния для результатов задания.</span><span class="sxs-lookup"><span data-stu-id="c010a-148">Specifies a state filter for the job results.</span></span>
<span data-ttu-id="c010a-149">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c010a-149">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c010a-150">Сохраняются</span><span class="sxs-lookup"><span data-stu-id="c010a-150">Accepted</span></span>
- <span data-ttu-id="c010a-151">Новые функции</span><span class="sxs-lookup"><span data-stu-id="c010a-151">New</span></span>
- <span data-ttu-id="c010a-152">Компиляция</span><span class="sxs-lookup"><span data-stu-id="c010a-152">Compiling</span></span>
- <span data-ttu-id="c010a-153">Планированию</span><span class="sxs-lookup"><span data-stu-id="c010a-153">Scheduling</span></span>
- <span data-ttu-id="c010a-154">Очереди</span><span class="sxs-lookup"><span data-stu-id="c010a-154">Queued</span></span>
- <span data-ttu-id="c010a-155">Начало</span><span class="sxs-lookup"><span data-stu-id="c010a-155">Starting</span></span>
- <span data-ttu-id="c010a-156">Приостановлено</span><span class="sxs-lookup"><span data-stu-id="c010a-156">Paused</span></span>
- <span data-ttu-id="c010a-157">Использующ</span><span class="sxs-lookup"><span data-stu-id="c010a-157">Running</span></span>
- <span data-ttu-id="c010a-158">Завершившихся</span><span class="sxs-lookup"><span data-stu-id="c010a-158">Ended</span></span>

```yaml
Type: JobState[]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 
Accepted values: Accepted, Compiling, Ended, New, Queued, Running, Scheduling, Starting, Paused, WaitingForCapacity

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c010a-159">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="c010a-159">-SubmittedAfter</span></span>
<span data-ttu-id="c010a-160">Задает фильтр по дате.</span><span class="sxs-lookup"><span data-stu-id="c010a-160">Specifies a date filter.</span></span>
<span data-ttu-id="c010a-161">Используйте этот параметр, чтобы отфильтровать результаты списка заданий, отправленных после указанной даты.</span><span class="sxs-lookup"><span data-stu-id="c010a-161">Use this parameter to filter the job list result to jobs submitted after the specified date.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c010a-162">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="c010a-162">-SubmittedBefore</span></span>
<span data-ttu-id="c010a-163">Задает фильтр по дате.</span><span class="sxs-lookup"><span data-stu-id="c010a-163">Specifies a date filter.</span></span>
<span data-ttu-id="c010a-164">Используйте этот параметр, чтобы отфильтровать результаты списка заданий по заданиям, отправленным до указанной даты.</span><span class="sxs-lookup"><span data-stu-id="c010a-164">Use this parameter to filter the job list result to jobs submitted before the specified date.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c010a-165">-Отправитель</span><span class="sxs-lookup"><span data-stu-id="c010a-165">-Submitter</span></span>
<span data-ttu-id="c010a-166">Указывает адрес электронной почты пользователя.</span><span class="sxs-lookup"><span data-stu-id="c010a-166">Specifies the email address of a user.</span></span>
<span data-ttu-id="c010a-167">Используйте этот параметр, чтобы отфильтровать результаты списка заданий по заданиям, передаваемым указанным пользователем.</span><span class="sxs-lookup"><span data-stu-id="c010a-167">Use this parameter to filter the job list results to jobs submitted by a specified user.</span></span>

```yaml
Type: String
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c010a-168">-Top</span><span class="sxs-lookup"><span data-stu-id="c010a-168">-Top</span></span>
<span data-ttu-id="c010a-169">Необязательное значение, показывающее количество возвращаемых заданий.</span><span class="sxs-lookup"><span data-stu-id="c010a-169">An optional value which indicates the number of jobs to return.</span></span> <span data-ttu-id="c010a-170">Значение по умолчанию — 500</span><span class="sxs-lookup"><span data-stu-id="c010a-170">Default value is 500</span></span>

```yaml
Type: Int32
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c010a-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c010a-171">CommonParameters</span></span>
<span data-ttu-id="c010a-172">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c010a-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c010a-173">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c010a-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c010a-174">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c010a-174">INPUTS</span></span>

### <span data-ttu-id="c010a-175">GUID</span><span class="sxs-lookup"><span data-stu-id="c010a-175">Guid</span></span>
<span data-ttu-id="c010a-176">Параметр "JobId" принимает значение типа "GUID" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="c010a-176">Parameter 'JobId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="c010a-177">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c010a-177">OUTPUTS</span></span>

### <span data-ttu-id="c010a-178">JobInformation</span><span class="sxs-lookup"><span data-stu-id="c010a-178">JobInformation</span></span>
<span data-ttu-id="c010a-179">Сведения о заданных сведениях о задании</span><span class="sxs-lookup"><span data-stu-id="c010a-179">The specified job information details</span></span>

### <span data-ttu-id="c010a-180">Список<PSJobInformationBasic></span><span class="sxs-lookup"><span data-stu-id="c010a-180">List<PSJobInformationBasic></span></span>
<span data-ttu-id="c010a-181">Список заданий в указанной учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="c010a-181">The list of jobs in the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="c010a-182">Пуск</span><span class="sxs-lookup"><span data-stu-id="c010a-182">NOTES</span></span>

## <span data-ttu-id="c010a-183">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c010a-183">RELATED LINKS</span></span>

[<span data-ttu-id="c010a-184">Остановить-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c010a-184">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="c010a-185">Submit-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c010a-185">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="c010a-186">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c010a-186">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


