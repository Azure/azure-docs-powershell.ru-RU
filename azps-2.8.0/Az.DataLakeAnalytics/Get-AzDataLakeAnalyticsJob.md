---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A0293D80-5935-4D2C-AF11-2837FEC95760
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 73a9325ea4f1bc45eaaf2fb81796d526c7b95fea
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721391"
---
# <span data-ttu-id="03956-101">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="03956-101">Get-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="03956-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="03956-102">SYNOPSIS</span></span>
<span data-ttu-id="03956-103">Получает задание Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="03956-103">Gets a Data Lake Analytics job.</span></span>

## <span data-ttu-id="03956-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="03956-104">SYNTAX</span></span>

### <span data-ttu-id="03956-105">GetAllInResourceGroupAndAccount (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="03956-105">GetAllInResourceGroupAndAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJob [-Account] <String> [[-Name] <String>] [[-Submitter] <String>]
 [[-SubmittedAfter] <DateTimeOffset>] [[-SubmittedBefore] <DateTimeOffset>] [[-State] <JobState[]>]
 [[-Result] <JobResult[]>] [-Top <Int32>] [-PipelineId <Guid>] [-RecurrenceId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03956-106">GetBySpecificJobInformation</span><span class="sxs-lookup"><span data-stu-id="03956-106">GetBySpecificJobInformation</span></span>
```
Get-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-Include] <ExtendedJobData>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03956-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="03956-107">DESCRIPTION</span></span>
<span data-ttu-id="03956-108">Командлет **Get-AzDataLakeAnalyticsJob** получает задание Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="03956-108">The **Get-AzDataLakeAnalyticsJob** cmdlet gets an Azure Data Lake Analytics job.</span></span>
<span data-ttu-id="03956-109">Если задание не задано, этот командлет получает все задания.</span><span class="sxs-lookup"><span data-stu-id="03956-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="03956-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="03956-110">EXAMPLES</span></span>

### <span data-ttu-id="03956-111">Пример 1: получение указанного задания</span><span class="sxs-lookup"><span data-stu-id="03956-111">Example 1: Get a specified job</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJob -Account "contosoadla" -JobId $JobID01
```

<span data-ttu-id="03956-112">Эта команда получает задание с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="03956-112">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="03956-113">Пример 2: получение заданий, отправленных за последнюю неделю</span><span class="sxs-lookup"><span data-stu-id="03956-113">Example 2: Get jobs submitted in the past week</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJob -Account "contosoadla" -SubmittedAfter (Get-Date).AddDays(-7)
```

<span data-ttu-id="03956-114">Эта команда получает задания, отправленные за последнюю неделю.</span><span class="sxs-lookup"><span data-stu-id="03956-114">This command gets jobs submitted in the past week.</span></span>

## <span data-ttu-id="03956-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="03956-115">PARAMETERS</span></span>

### <span data-ttu-id="03956-116">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="03956-116">-Account</span></span>
<span data-ttu-id="03956-117">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="03956-117">Specifies the name of a Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="03956-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03956-118">-DefaultProfile</span></span>
<span data-ttu-id="03956-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="03956-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="03956-120">-Include</span><span class="sxs-lookup"><span data-stu-id="03956-120">-Include</span></span>
<span data-ttu-id="03956-121">Задает параметры, указывающие тип дополнительной информации, которую требуется получить о задании.</span><span class="sxs-lookup"><span data-stu-id="03956-121">Specifies options that indicate the type of additional information to retrieve about the job.</span></span>
<span data-ttu-id="03956-122">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="03956-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="03956-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="03956-123">None</span></span>
- <span data-ttu-id="03956-124">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="03956-124">DebugInfo</span></span>
- <span data-ttu-id="03956-125">Сведения</span><span class="sxs-lookup"><span data-stu-id="03956-125">Statistics</span></span>
- <span data-ttu-id="03956-126">Весь</span><span class="sxs-lookup"><span data-stu-id="03956-126">All</span></span>

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

### <span data-ttu-id="03956-127">-JobId</span><span class="sxs-lookup"><span data-stu-id="03956-127">-JobId</span></span>
<span data-ttu-id="03956-128">Указывает ИД задания, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="03956-128">Specifies the ID of the job to get.</span></span>

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

### <span data-ttu-id="03956-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="03956-129">-Name</span></span>
<span data-ttu-id="03956-130">Указывает имя, которое будет использоваться для фильтрации результатов списка заданий.</span><span class="sxs-lookup"><span data-stu-id="03956-130">Specifies a name to use to filter the job list results.</span></span>
<span data-ttu-id="03956-131">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="03956-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="03956-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="03956-132">None</span></span>
- <span data-ttu-id="03956-133">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="03956-133">DebugInfo</span></span>
- <span data-ttu-id="03956-134">Сведения</span><span class="sxs-lookup"><span data-stu-id="03956-134">Statistics</span></span>
- <span data-ttu-id="03956-135">Весь</span><span class="sxs-lookup"><span data-stu-id="03956-135">All</span></span>

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

### <span data-ttu-id="03956-136">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="03956-136">-PipelineId</span></span>
<span data-ttu-id="03956-137">Необязательный идентификатор, указывающий на то, что должны возвращаться только задания, входящие в указанный конвейер.</span><span class="sxs-lookup"><span data-stu-id="03956-137">An optional ID that indicates only jobs part of the specified pipeline should be returned.</span></span>

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

### <span data-ttu-id="03956-138">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="03956-138">-RecurrenceId</span></span>
<span data-ttu-id="03956-139">Необязательный идентификатор, указывающий на то, что должны возвращаться только задания, входящие в указанное повторение.</span><span class="sxs-lookup"><span data-stu-id="03956-139">An optional ID that indicates only jobs part of the specified recurrence should be returned.</span></span>

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

### <span data-ttu-id="03956-140">-Result (результат)</span><span class="sxs-lookup"><span data-stu-id="03956-140">-Result</span></span>
<span data-ttu-id="03956-141">Указывает фильтр результатов для результатов задания.</span><span class="sxs-lookup"><span data-stu-id="03956-141">Specifies a result filter for the job results.</span></span>
<span data-ttu-id="03956-142">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="03956-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="03956-143">Ничего</span><span class="sxs-lookup"><span data-stu-id="03956-143">None</span></span>
- <span data-ttu-id="03956-144">Отменен</span><span class="sxs-lookup"><span data-stu-id="03956-144">Cancelled</span></span>
- <span data-ttu-id="03956-145">Ошибкой</span><span class="sxs-lookup"><span data-stu-id="03956-145">Failed</span></span>
- <span data-ttu-id="03956-146">LSP</span><span class="sxs-lookup"><span data-stu-id="03956-146">Succeeded</span></span>

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

### <span data-ttu-id="03956-147">-State</span><span class="sxs-lookup"><span data-stu-id="03956-147">-State</span></span>
<span data-ttu-id="03956-148">Указывает фильтр состояния для результатов задания.</span><span class="sxs-lookup"><span data-stu-id="03956-148">Specifies a state filter for the job results.</span></span>
<span data-ttu-id="03956-149">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="03956-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="03956-150">Сохраняются</span><span class="sxs-lookup"><span data-stu-id="03956-150">Accepted</span></span>
- <span data-ttu-id="03956-151">Новые функции</span><span class="sxs-lookup"><span data-stu-id="03956-151">New</span></span>
- <span data-ttu-id="03956-152">Компиляция</span><span class="sxs-lookup"><span data-stu-id="03956-152">Compiling</span></span>
- <span data-ttu-id="03956-153">Планированию</span><span class="sxs-lookup"><span data-stu-id="03956-153">Scheduling</span></span>
- <span data-ttu-id="03956-154">Очереди</span><span class="sxs-lookup"><span data-stu-id="03956-154">Queued</span></span>
- <span data-ttu-id="03956-155">Начало</span><span class="sxs-lookup"><span data-stu-id="03956-155">Starting</span></span>
- <span data-ttu-id="03956-156">Приостановлено</span><span class="sxs-lookup"><span data-stu-id="03956-156">Paused</span></span>
- <span data-ttu-id="03956-157">Использующ</span><span class="sxs-lookup"><span data-stu-id="03956-157">Running</span></span>
- <span data-ttu-id="03956-158">Завершившихся</span><span class="sxs-lookup"><span data-stu-id="03956-158">Ended</span></span>

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

### <span data-ttu-id="03956-159">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="03956-159">-SubmittedAfter</span></span>
<span data-ttu-id="03956-160">Задает фильтр по дате.</span><span class="sxs-lookup"><span data-stu-id="03956-160">Specifies a date filter.</span></span>
<span data-ttu-id="03956-161">Используйте этот параметр, чтобы отфильтровать результаты списка заданий, отправленных после указанной даты.</span><span class="sxs-lookup"><span data-stu-id="03956-161">Use this parameter to filter the job list result to jobs submitted after the specified date.</span></span>

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

### <span data-ttu-id="03956-162">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="03956-162">-SubmittedBefore</span></span>
<span data-ttu-id="03956-163">Задает фильтр по дате.</span><span class="sxs-lookup"><span data-stu-id="03956-163">Specifies a date filter.</span></span>
<span data-ttu-id="03956-164">Используйте этот параметр, чтобы отфильтровать результаты списка заданий по заданиям, отправленным до указанной даты.</span><span class="sxs-lookup"><span data-stu-id="03956-164">Use this parameter to filter the job list result to jobs submitted before the specified date.</span></span>

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

### <span data-ttu-id="03956-165">-Отправитель</span><span class="sxs-lookup"><span data-stu-id="03956-165">-Submitter</span></span>
<span data-ttu-id="03956-166">Указывает адрес электронной почты пользователя.</span><span class="sxs-lookup"><span data-stu-id="03956-166">Specifies the email address of a user.</span></span>
<span data-ttu-id="03956-167">Используйте этот параметр, чтобы отфильтровать результаты списка заданий по заданиям, передаваемым указанным пользователем.</span><span class="sxs-lookup"><span data-stu-id="03956-167">Use this parameter to filter the job list results to jobs submitted by a specified user.</span></span>

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

### <span data-ttu-id="03956-168">-Top</span><span class="sxs-lookup"><span data-stu-id="03956-168">-Top</span></span>
<span data-ttu-id="03956-169">Необязательное значение, показывающее количество возвращаемых заданий.</span><span class="sxs-lookup"><span data-stu-id="03956-169">An optional value which indicates the number of jobs to return.</span></span> <span data-ttu-id="03956-170">Значение по умолчанию — 500</span><span class="sxs-lookup"><span data-stu-id="03956-170">Default value is 500</span></span>

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

### <span data-ttu-id="03956-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03956-171">CommonParameters</span></span>
<span data-ttu-id="03956-172">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="03956-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03956-173">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03956-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03956-174">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="03956-174">INPUTS</span></span>

### <span data-ttu-id="03956-175">System. String</span><span class="sxs-lookup"><span data-stu-id="03956-175">System.String</span></span>

### <span data-ttu-id="03956-176">System. GUID</span><span class="sxs-lookup"><span data-stu-id="03956-176">System.Guid</span></span>

### <span data-ttu-id="03956-177">Microsoft. Azure. Commands. DataLakeAnalytics. Models. DataLakeAnalyticsEnums + ExtendedJobData</span><span class="sxs-lookup"><span data-stu-id="03956-177">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData</span></span>

### <span data-ttu-id="03956-178">System. Nullable "1 [[System. DateTimeOffset, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="03956-178">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="03956-179">Microsoft. Azure. Management. Lake. Analytics. Models. JobState []</span><span class="sxs-lookup"><span data-stu-id="03956-179">Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]</span></span>

### <span data-ttu-id="03956-180">Microsoft. Azure. Management. Lake. Analytics. Models. JobResult []</span><span class="sxs-lookup"><span data-stu-id="03956-180">Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]</span></span>

### <span data-ttu-id="03956-181">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="03956-181">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="03956-182">System. Nullable "1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="03956-182">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="03956-183">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="03956-183">OUTPUTS</span></span>

### <span data-ttu-id="03956-184">Microsoft. Azure. Management. данных Lake. Analytics. Models. JobInformation</span><span class="sxs-lookup"><span data-stu-id="03956-184">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="03956-185">Пуск</span><span class="sxs-lookup"><span data-stu-id="03956-185">NOTES</span></span>

## <span data-ttu-id="03956-186">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="03956-186">RELATED LINKS</span></span>

[<span data-ttu-id="03956-187">Остановить-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="03956-187">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="03956-188">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="03956-188">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="03956-189">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="03956-189">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)


