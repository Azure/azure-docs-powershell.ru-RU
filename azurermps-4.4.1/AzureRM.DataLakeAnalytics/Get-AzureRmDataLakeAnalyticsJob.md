---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A0293D80-5935-4D2C-AF11-2837FEC95760
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: 6a172de918e8b0675abaf01edf2ec198dae75b5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569540"
---
# <span data-ttu-id="18bf1-101">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="18bf1-101">Get-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="18bf1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="18bf1-102">SYNOPSIS</span></span>
<span data-ttu-id="18bf1-103">Получает задание Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="18bf1-103">Gets a Data Lake Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18bf1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="18bf1-104">SYNTAX</span></span>

### <span data-ttu-id="18bf1-105">Все в группе ресурсов и в учетной записи (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="18bf1-105">All In Resource Group and Account (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [[-Name] <String>] [[-Submitter] <String>]
 [[-SubmittedAfter] <DateTimeOffset>] [[-SubmittedBefore] <DateTimeOffset>] [[-State] <JobState[]>]
 [[-Result] <JobResult[]>] [-Top <Int32>] [-PipelineId <Guid>] [-RecurrenceId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18bf1-106">Конкретные JobInformation</span><span class="sxs-lookup"><span data-stu-id="18bf1-106">Specific JobInformation</span></span>
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-Include] <ExtendedJobData>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18bf1-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="18bf1-107">DESCRIPTION</span></span>
<span data-ttu-id="18bf1-108">Командлет **Get-AzureRmDataLakeAnalyticsJob** получает задание Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="18bf1-108">The **Get-AzureRmDataLakeAnalyticsJob** cmdlet gets an Azure Data Lake Analytics job.</span></span>
<span data-ttu-id="18bf1-109">Если задание не задано, этот командлет получает все задания.</span><span class="sxs-lookup"><span data-stu-id="18bf1-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="18bf1-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="18bf1-110">EXAMPLES</span></span>

### <span data-ttu-id="18bf1-111">Пример 1: получение указанного задания</span><span class="sxs-lookup"><span data-stu-id="18bf1-111">Example 1: Get a specified job</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -JobId $JobID01
```

<span data-ttu-id="18bf1-112">Эта команда получает задание с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="18bf1-112">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="18bf1-113">Пример 2: получение заданий, отправленных за последнюю неделю</span><span class="sxs-lookup"><span data-stu-id="18bf1-113">Example 2: Get jobs submitted in the past week</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -SubmittedAfter (Get-Date).AddDays(-7)
```

<span data-ttu-id="18bf1-114">Эта команда получает задания, отправленные за последнюю неделю.</span><span class="sxs-lookup"><span data-stu-id="18bf1-114">This command gets jobs submitted in the past week.</span></span>

## <span data-ttu-id="18bf1-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="18bf1-115">PARAMETERS</span></span>

### <span data-ttu-id="18bf1-116">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="18bf1-116">-Account</span></span>
<span data-ttu-id="18bf1-117">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="18bf1-117">Specifies the name of a Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18bf1-118">-Include</span><span class="sxs-lookup"><span data-stu-id="18bf1-118">-Include</span></span>
<span data-ttu-id="18bf1-119">Задает параметры, указывающие тип дополнительной информации, которую требуется получить о задании.</span><span class="sxs-lookup"><span data-stu-id="18bf1-119">Specifies options that indicate the type of additional information to retrieve about the job.</span></span>
<span data-ttu-id="18bf1-120">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="18bf1-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="18bf1-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="18bf1-121">None</span></span>
- <span data-ttu-id="18bf1-122">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="18bf1-122">DebugInfo</span></span>
- <span data-ttu-id="18bf1-123">Сведения</span><span class="sxs-lookup"><span data-stu-id="18bf1-123">Statistics</span></span>
- <span data-ttu-id="18bf1-124">Весь</span><span class="sxs-lookup"><span data-stu-id="18bf1-124">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData
Parameter Sets: Specific JobInformation
Aliases: 
Accepted values: None, All, DebugInfo, Statistics

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18bf1-125">-JobId</span><span class="sxs-lookup"><span data-stu-id="18bf1-125">-JobId</span></span>
<span data-ttu-id="18bf1-126">Указывает ИД задания, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="18bf1-126">Specifies the ID of the job to get.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Specific JobInformation
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18bf1-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="18bf1-127">-Name</span></span>
<span data-ttu-id="18bf1-128">Указывает имя, которое будет использоваться для фильтрации результатов списка заданий.</span><span class="sxs-lookup"><span data-stu-id="18bf1-128">Specifies a name to use to filter the job list results.</span></span>
<span data-ttu-id="18bf1-129">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="18bf1-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="18bf1-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="18bf1-130">None</span></span>
- <span data-ttu-id="18bf1-131">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="18bf1-131">DebugInfo</span></span>
- <span data-ttu-id="18bf1-132">Сведения</span><span class="sxs-lookup"><span data-stu-id="18bf1-132">Statistics</span></span>
- <span data-ttu-id="18bf1-133">Весь</span><span class="sxs-lookup"><span data-stu-id="18bf1-133">All</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18bf1-134">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="18bf1-134">-PipelineId</span></span>
<span data-ttu-id="18bf1-135">Необязательный идентификатор, указывающий на то, что должны возвращаться только задания, входящие в указанный конвейер.</span><span class="sxs-lookup"><span data-stu-id="18bf1-135">An optional ID that indicates only jobs part of the specified pipeline should be returned.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18bf1-136">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="18bf1-136">-RecurrenceId</span></span>
<span data-ttu-id="18bf1-137">Необязательный идентификатор, указывающий на то, что должны возвращаться только задания, входящие в указанное повторение.</span><span class="sxs-lookup"><span data-stu-id="18bf1-137">An optional ID that indicates only jobs part of the specified recurrence should be returned.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18bf1-138">-Result (результат)</span><span class="sxs-lookup"><span data-stu-id="18bf1-138">-Result</span></span>
<span data-ttu-id="18bf1-139">Указывает фильтр результатов для результатов задания.</span><span class="sxs-lookup"><span data-stu-id="18bf1-139">Specifies a result filter for the job results.</span></span>
<span data-ttu-id="18bf1-140">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="18bf1-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="18bf1-141">Ничего</span><span class="sxs-lookup"><span data-stu-id="18bf1-141">None</span></span>
- <span data-ttu-id="18bf1-142">Отменен</span><span class="sxs-lookup"><span data-stu-id="18bf1-142">Cancelled</span></span>
- <span data-ttu-id="18bf1-143">Ошибкой</span><span class="sxs-lookup"><span data-stu-id="18bf1-143">Failed</span></span>
- <span data-ttu-id="18bf1-144">LSP</span><span class="sxs-lookup"><span data-stu-id="18bf1-144">Succeeded</span></span>

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]
Parameter Sets: All In Resource Group and Account
Aliases: 
Accepted values: None, Succeeded, Cancelled, Failed

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18bf1-145">-State</span><span class="sxs-lookup"><span data-stu-id="18bf1-145">-State</span></span>
<span data-ttu-id="18bf1-146">Указывает фильтр состояния для результатов задания.</span><span class="sxs-lookup"><span data-stu-id="18bf1-146">Specifies a state filter for the job results.</span></span>
<span data-ttu-id="18bf1-147">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="18bf1-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="18bf1-148">Сохраняются</span><span class="sxs-lookup"><span data-stu-id="18bf1-148">Accepted</span></span>
- <span data-ttu-id="18bf1-149">Новые функции</span><span class="sxs-lookup"><span data-stu-id="18bf1-149">New</span></span>
- <span data-ttu-id="18bf1-150">Компиляция</span><span class="sxs-lookup"><span data-stu-id="18bf1-150">Compiling</span></span>
- <span data-ttu-id="18bf1-151">Планированию</span><span class="sxs-lookup"><span data-stu-id="18bf1-151">Scheduling</span></span>
- <span data-ttu-id="18bf1-152">Очереди</span><span class="sxs-lookup"><span data-stu-id="18bf1-152">Queued</span></span>
- <span data-ttu-id="18bf1-153">Начало</span><span class="sxs-lookup"><span data-stu-id="18bf1-153">Starting</span></span>
- <span data-ttu-id="18bf1-154">Приостановлено</span><span class="sxs-lookup"><span data-stu-id="18bf1-154">Paused</span></span>
- <span data-ttu-id="18bf1-155">Использующ</span><span class="sxs-lookup"><span data-stu-id="18bf1-155">Running</span></span>
- <span data-ttu-id="18bf1-156">Завершившихся</span><span class="sxs-lookup"><span data-stu-id="18bf1-156">Ended</span></span>

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]
Parameter Sets: All In Resource Group and Account
Aliases: 
Accepted values: Accepted, Compiling, Ended, New, Queued, Running, Scheduling, Starting, Paused, WaitingForCapacity

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18bf1-157">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="18bf1-157">-SubmittedAfter</span></span>
<span data-ttu-id="18bf1-158">Задает фильтр по дате.</span><span class="sxs-lookup"><span data-stu-id="18bf1-158">Specifies a date filter.</span></span>
<span data-ttu-id="18bf1-159">Используйте этот параметр, чтобы отфильтровать результаты списка заданий, отправленных после указанной даты.</span><span class="sxs-lookup"><span data-stu-id="18bf1-159">Use this parameter to filter the job list result to jobs submitted after the specified date.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18bf1-160">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="18bf1-160">-SubmittedBefore</span></span>
<span data-ttu-id="18bf1-161">Задает фильтр по дате.</span><span class="sxs-lookup"><span data-stu-id="18bf1-161">Specifies a date filter.</span></span>
<span data-ttu-id="18bf1-162">Используйте этот параметр, чтобы отфильтровать результаты списка заданий по заданиям, отправленным до указанной даты.</span><span class="sxs-lookup"><span data-stu-id="18bf1-162">Use this parameter to filter the job list result to jobs submitted before the specified date.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18bf1-163">-Отправитель</span><span class="sxs-lookup"><span data-stu-id="18bf1-163">-Submitter</span></span>
<span data-ttu-id="18bf1-164">Указывает адрес электронной почты пользователя.</span><span class="sxs-lookup"><span data-stu-id="18bf1-164">Specifies the email address of a user.</span></span>
<span data-ttu-id="18bf1-165">Используйте этот параметр, чтобы отфильтровать результаты списка заданий по заданиям, передаваемым указанным пользователем.</span><span class="sxs-lookup"><span data-stu-id="18bf1-165">Use this parameter to filter the job list results to jobs submitted by a specified user.</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18bf1-166">-Top</span><span class="sxs-lookup"><span data-stu-id="18bf1-166">-Top</span></span>
<span data-ttu-id="18bf1-167">Необязательное значение, показывающее количество возвращаемых заданий.</span><span class="sxs-lookup"><span data-stu-id="18bf1-167">An optional value which indicates the number of jobs to return.</span></span> <span data-ttu-id="18bf1-168">Значение по умолчанию — 500</span><span class="sxs-lookup"><span data-stu-id="18bf1-168">Default value is 500</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18bf1-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18bf1-169">-DefaultProfile</span></span>
<span data-ttu-id="18bf1-170">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="18bf1-170">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18bf1-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18bf1-171">CommonParameters</span></span>
<span data-ttu-id="18bf1-172">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="18bf1-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18bf1-173">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18bf1-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18bf1-174">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="18bf1-174">INPUTS</span></span>

### <span data-ttu-id="18bf1-175">GUID</span><span class="sxs-lookup"><span data-stu-id="18bf1-175">Guid</span></span>
<span data-ttu-id="18bf1-176">Параметр "JobId" принимает значение типа "GUID" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="18bf1-176">Parameter 'JobId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="18bf1-177">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="18bf1-177">OUTPUTS</span></span>

### <span data-ttu-id="18bf1-178">JobInformation</span><span class="sxs-lookup"><span data-stu-id="18bf1-178">JobInformation</span></span>
<span data-ttu-id="18bf1-179">Сведения о заданных сведениях о задании</span><span class="sxs-lookup"><span data-stu-id="18bf1-179">The specified job information details</span></span>

### <span data-ttu-id="18bf1-180">Список<JobInformation></span><span class="sxs-lookup"><span data-stu-id="18bf1-180">List<JobInformation></span></span>
<span data-ttu-id="18bf1-181">Список заданий в указанной учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="18bf1-181">The list of jobs in the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="18bf1-182">Пуск</span><span class="sxs-lookup"><span data-stu-id="18bf1-182">NOTES</span></span>

## <span data-ttu-id="18bf1-183">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="18bf1-183">RELATED LINKS</span></span>

[<span data-ttu-id="18bf1-184">Остановить-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="18bf1-184">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="18bf1-185">Submit-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="18bf1-185">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="18bf1-186">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="18bf1-186">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


