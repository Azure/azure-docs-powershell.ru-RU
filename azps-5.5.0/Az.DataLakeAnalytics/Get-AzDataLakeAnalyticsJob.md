---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A0293D80-5935-4D2C-AF11-2837FEC95760
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 02e0678b9c86643df9cd4bfc2192908ed4748249
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100215017"
---
# <span data-ttu-id="f76b3-101">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f76b3-101">Get-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="f76b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f76b3-102">SYNOPSIS</span></span>
<span data-ttu-id="f76b3-103">Получает задание анализа для data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="f76b3-103">Gets a Data Lake Analytics job.</span></span>

## <span data-ttu-id="f76b3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f76b3-104">SYNTAX</span></span>

### <span data-ttu-id="f76b3-105">GetAllInResourceGroupAndAccount (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f76b3-105">GetAllInResourceGroupAndAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJob [-Account] <String> [[-Name] <String>] [[-Submitter] <String>]
 [[-SubmittedAfter] <DateTimeOffset>] [[-SubmittedBefore] <DateTimeOffset>] [[-State] <JobState[]>]
 [[-Result] <JobResult[]>] [-Top <Int32>] [-PipelineId <Guid>] [-RecurrenceId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f76b3-106">GetBySpecificJobInformation</span><span class="sxs-lookup"><span data-stu-id="f76b3-106">GetBySpecificJobInformation</span></span>
```
Get-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-Include] <ExtendedJobData>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f76b3-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f76b3-107">DESCRIPTION</span></span>
<span data-ttu-id="f76b3-108">Для **работы с данными Azure Data Lake Analytics задание get-AzDataLakeAnalyticsJob.**</span><span class="sxs-lookup"><span data-stu-id="f76b3-108">The **Get-AzDataLakeAnalyticsJob** cmdlet gets an Azure Data Lake Analytics job.</span></span>
<span data-ttu-id="f76b3-109">Если задание не указано, этот cmdlet получает все задания.</span><span class="sxs-lookup"><span data-stu-id="f76b3-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="f76b3-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f76b3-110">EXAMPLES</span></span>

### <span data-ttu-id="f76b3-111">Пример 1. Получить задание</span><span class="sxs-lookup"><span data-stu-id="f76b3-111">Example 1: Get a specified job</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJob -Account "contosoadla" -JobId $JobID01
```

<span data-ttu-id="f76b3-112">Эта команда получает задание с указанным ид.</span><span class="sxs-lookup"><span data-stu-id="f76b3-112">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="f76b3-113">Пример 2. Отправка заданий за прошедшую неделю</span><span class="sxs-lookup"><span data-stu-id="f76b3-113">Example 2: Get jobs submitted in the past week</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJob -Account "contosoadla" -SubmittedAfter (Get-Date).AddDays(-7)
```

<span data-ttu-id="f76b3-114">Эта команда получает задания за прошедшую неделю.</span><span class="sxs-lookup"><span data-stu-id="f76b3-114">This command gets jobs submitted in the past week.</span></span>

## <span data-ttu-id="f76b3-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f76b3-115">PARAMETERS</span></span>

### <span data-ttu-id="f76b3-116">-Account</span><span class="sxs-lookup"><span data-stu-id="f76b3-116">-Account</span></span>
<span data-ttu-id="f76b3-117">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="f76b3-117">Specifies the name of a Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="f76b3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f76b3-118">-DefaultProfile</span></span>
<span data-ttu-id="f76b3-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f76b3-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f76b3-120">-Include</span><span class="sxs-lookup"><span data-stu-id="f76b3-120">-Include</span></span>
<span data-ttu-id="f76b3-121">Определяет параметры, которые указывают на тип дополнительных сведений, которые необходимо получить о задаче.</span><span class="sxs-lookup"><span data-stu-id="f76b3-121">Specifies options that indicate the type of additional information to retrieve about the job.</span></span>
<span data-ttu-id="f76b3-122">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="f76b3-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f76b3-123">Нет</span><span class="sxs-lookup"><span data-stu-id="f76b3-123">None</span></span>
- <span data-ttu-id="f76b3-124">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="f76b3-124">DebugInfo</span></span>
- <span data-ttu-id="f76b3-125">Статистика</span><span class="sxs-lookup"><span data-stu-id="f76b3-125">Statistics</span></span>
- <span data-ttu-id="f76b3-126">Все</span><span class="sxs-lookup"><span data-stu-id="f76b3-126">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData
Parameter Sets: GetBySpecificJobInformation
Aliases:
Accepted values: None, All, DebugInfo, Statistics

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f76b3-127">-JobId</span><span class="sxs-lookup"><span data-stu-id="f76b3-127">-JobId</span></span>
<span data-ttu-id="f76b3-128">Определяет ИД задания, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="f76b3-128">Specifies the ID of the job to get.</span></span>

```yaml
Type: System.Guid
Parameter Sets: GetBySpecificJobInformation
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f76b3-129">-Name</span><span class="sxs-lookup"><span data-stu-id="f76b3-129">-Name</span></span>
<span data-ttu-id="f76b3-130">Указывает имя, которое будет использовать для фильтрации результатов списка задания.</span><span class="sxs-lookup"><span data-stu-id="f76b3-130">Specifies a name to use to filter the job list results.</span></span>
<span data-ttu-id="f76b3-131">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="f76b3-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f76b3-132">Нет</span><span class="sxs-lookup"><span data-stu-id="f76b3-132">None</span></span>
- <span data-ttu-id="f76b3-133">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="f76b3-133">DebugInfo</span></span>
- <span data-ttu-id="f76b3-134">Статистика</span><span class="sxs-lookup"><span data-stu-id="f76b3-134">Statistics</span></span>
- <span data-ttu-id="f76b3-135">Все</span><span class="sxs-lookup"><span data-stu-id="f76b3-135">All</span></span>

```yaml
Type: System.String
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f76b3-136">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="f76b3-136">-PipelineId</span></span>
<span data-ttu-id="f76b3-137">Должен быть возвращен необязательный ИД, который указывает только часть указанного конвейера заданий.</span><span class="sxs-lookup"><span data-stu-id="f76b3-137">An optional ID that indicates only jobs part of the specified pipeline should be returned.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f76b3-138">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="f76b3-138">-RecurrenceId</span></span>
<span data-ttu-id="f76b3-139">Должен быть возвращен необязательный ИД, который указывает только часть указанного повторения.</span><span class="sxs-lookup"><span data-stu-id="f76b3-139">An optional ID that indicates only jobs part of the specified recurrence should be returned.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f76b3-140">-Результат</span><span class="sxs-lookup"><span data-stu-id="f76b3-140">-Result</span></span>
<span data-ttu-id="f76b3-141">Фильтр результатов для результатов задания.</span><span class="sxs-lookup"><span data-stu-id="f76b3-141">Specifies a result filter for the job results.</span></span>
<span data-ttu-id="f76b3-142">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="f76b3-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f76b3-143">Нет</span><span class="sxs-lookup"><span data-stu-id="f76b3-143">None</span></span>
- <span data-ttu-id="f76b3-144">Отменено</span><span class="sxs-lookup"><span data-stu-id="f76b3-144">Cancelled</span></span>
- <span data-ttu-id="f76b3-145">Сбой</span><span class="sxs-lookup"><span data-stu-id="f76b3-145">Failed</span></span>
- <span data-ttu-id="f76b3-146">Успешно</span><span class="sxs-lookup"><span data-stu-id="f76b3-146">Succeeded</span></span>

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:
Accepted values: None, Succeeded, Cancelled, Failed

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f76b3-147">-State</span><span class="sxs-lookup"><span data-stu-id="f76b3-147">-State</span></span>
<span data-ttu-id="f76b3-148">Определяет фильтр штата для результатов задания.</span><span class="sxs-lookup"><span data-stu-id="f76b3-148">Specifies a state filter for the job results.</span></span>
<span data-ttu-id="f76b3-149">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="f76b3-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f76b3-150">Принято</span><span class="sxs-lookup"><span data-stu-id="f76b3-150">Accepted</span></span>
- <span data-ttu-id="f76b3-151">Новые функции</span><span class="sxs-lookup"><span data-stu-id="f76b3-151">New</span></span>
- <span data-ttu-id="f76b3-152">Компилялятор</span><span class="sxs-lookup"><span data-stu-id="f76b3-152">Compiling</span></span>
- <span data-ttu-id="f76b3-153">Планирование</span><span class="sxs-lookup"><span data-stu-id="f76b3-153">Scheduling</span></span>
- <span data-ttu-id="f76b3-154">В очереди</span><span class="sxs-lookup"><span data-stu-id="f76b3-154">Queued</span></span>
- <span data-ttu-id="f76b3-155">Запуск</span><span class="sxs-lookup"><span data-stu-id="f76b3-155">Starting</span></span>
- <span data-ttu-id="f76b3-156">Приостановлено</span><span class="sxs-lookup"><span data-stu-id="f76b3-156">Paused</span></span>
- <span data-ttu-id="f76b3-157">Запущена</span><span class="sxs-lookup"><span data-stu-id="f76b3-157">Running</span></span>
- <span data-ttu-id="f76b3-158">Завершено</span><span class="sxs-lookup"><span data-stu-id="f76b3-158">Ended</span></span>

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:
Accepted values: Accepted, Compiling, Ended, New, Queued, Running, Scheduling, Starting, Paused, WaitingForCapacity

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f76b3-159">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="f76b3-159">-SubmittedAfter</span></span>
<span data-ttu-id="f76b3-160">Определяет фильтр по дате.</span><span class="sxs-lookup"><span data-stu-id="f76b3-160">Specifies a date filter.</span></span>
<span data-ttu-id="f76b3-161">Используйте этот параметр, чтобы отфильтровать результаты списка заданий по заданиям, отправленным после указанной даты.</span><span class="sxs-lookup"><span data-stu-id="f76b3-161">Use this parameter to filter the job list result to jobs submitted after the specified date.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f76b3-162">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="f76b3-162">-SubmittedBefore</span></span>
<span data-ttu-id="f76b3-163">Определяет фильтр по дате.</span><span class="sxs-lookup"><span data-stu-id="f76b3-163">Specifies a date filter.</span></span>
<span data-ttu-id="f76b3-164">Используйте этот параметр, чтобы отфильтровать результаты списка заданий по заданиям, отправленным до указанной даты.</span><span class="sxs-lookup"><span data-stu-id="f76b3-164">Use this parameter to filter the job list result to jobs submitted before the specified date.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f76b3-165">-Submitter</span><span class="sxs-lookup"><span data-stu-id="f76b3-165">-Submitter</span></span>
<span data-ttu-id="f76b3-166">Определяет адрес электронной почты пользователя.</span><span class="sxs-lookup"><span data-stu-id="f76b3-166">Specifies the email address of a user.</span></span>
<span data-ttu-id="f76b3-167">Используйте этот параметр, чтобы фильтровать результаты списка заданий по заданиям, отправленным указанным пользователем.</span><span class="sxs-lookup"><span data-stu-id="f76b3-167">Use this parameter to filter the job list results to jobs submitted by a specified user.</span></span>

```yaml
Type: System.String
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f76b3-168">-Top</span><span class="sxs-lookup"><span data-stu-id="f76b3-168">-Top</span></span>
<span data-ttu-id="f76b3-169">Необязательное значение, которое указывает количество возвращаемого задания.</span><span class="sxs-lookup"><span data-stu-id="f76b3-169">An optional value which indicates the number of jobs to return.</span></span> <span data-ttu-id="f76b3-170">Значение по умолчанию — 500</span><span class="sxs-lookup"><span data-stu-id="f76b3-170">Default value is 500</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f76b3-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f76b3-171">CommonParameters</span></span>
<span data-ttu-id="f76b3-172">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f76b3-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f76b3-173">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f76b3-173">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f76b3-174">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f76b3-174">INPUTS</span></span>

### <span data-ttu-id="f76b3-175">System.String</span><span class="sxs-lookup"><span data-stu-id="f76b3-175">System.String</span></span>

### <span data-ttu-id="f76b3-176">System.Guid</span><span class="sxs-lookup"><span data-stu-id="f76b3-176">System.Guid</span></span>

### <span data-ttu-id="f76b3-177">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData</span><span class="sxs-lookup"><span data-stu-id="f76b3-177">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData</span></span>

### <span data-ttu-id="f76b3-178">System.Nullable'1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f76b3-178">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="f76b3-179">Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]</span><span class="sxs-lookup"><span data-stu-id="f76b3-179">Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]</span></span>

### <span data-ttu-id="f76b3-180">Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]</span><span class="sxs-lookup"><span data-stu-id="f76b3-180">Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]</span></span>

### <span data-ttu-id="f76b3-181">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f76b3-181">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="f76b3-182">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f76b3-182">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f76b3-183">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f76b3-183">OUTPUTS</span></span>

### <span data-ttu-id="f76b3-184">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span><span class="sxs-lookup"><span data-stu-id="f76b3-184">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="f76b3-185">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f76b3-185">NOTES</span></span>

## <span data-ttu-id="f76b3-186">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f76b3-186">RELATED LINKS</span></span>

[<span data-ttu-id="f76b3-187">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f76b3-187">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="f76b3-188">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f76b3-188">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="f76b3-189">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f76b3-189">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)


