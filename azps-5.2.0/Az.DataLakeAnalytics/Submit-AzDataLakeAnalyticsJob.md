---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0DB9595A-6C8B-4F3F-A707-2DB41D7C7470
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/submit-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Submit-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Submit-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 2fcd30c523508620d7d7ed20ebce60facc2678a0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401359"
---
# <span data-ttu-id="eb9dc-101">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="eb9dc-101">Submit-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="eb9dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb9dc-102">SYNOPSIS</span></span>
<span data-ttu-id="eb9dc-103">Отправка задания.</span><span class="sxs-lookup"><span data-stu-id="eb9dc-103">Submits a job.</span></span>

## <span data-ttu-id="eb9dc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="eb9dc-104">SYNTAX</span></span>

### <span data-ttu-id="eb9dc-105">SubmitUSqlJobWithScriptPath</span><span class="sxs-lookup"><span data-stu-id="eb9dc-105">SubmitUSqlJobWithScriptPath</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb9dc-106">SubmitUSqlJob</span><span class="sxs-lookup"><span data-stu-id="eb9dc-106">SubmitUSqlJob</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb9dc-107">SubmitUSqlJobWithScriptPathAndRecurrence</span><span class="sxs-lookup"><span data-stu-id="eb9dc-107">SubmitUSqlJobWithScriptPathAndRecurrence</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb9dc-108">SubmitUSqlJobWithRecurrence</span><span class="sxs-lookup"><span data-stu-id="eb9dc-108">SubmitUSqlJobWithRecurrence</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb9dc-109">SubmitUSqlJobWithScriptPathAndPipeline</span><span class="sxs-lookup"><span data-stu-id="eb9dc-109">SubmitUSqlJobWithScriptPathAndPipeline</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eb9dc-110">SubmitUSqlJobWithPipeline</span><span class="sxs-lookup"><span data-stu-id="eb9dc-110">SubmitUSqlJobWithPipeline</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eb9dc-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb9dc-111">DESCRIPTION</span></span>
<span data-ttu-id="eb9dc-112">**Cmdlet Submit-AzDataLakeAnalyticsJob** представляет задание Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="eb9dc-112">The **Submit-AzDataLakeAnalyticsJob** cmdlet submits an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="eb9dc-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="eb9dc-113">EXAMPLES</span></span>

### <span data-ttu-id="eb9dc-114">Пример 1. Отправка задания</span><span class="sxs-lookup"><span data-stu-id="eb9dc-114">Example 1: Submit a job</span></span>
```
PS C:\>Submit-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32
```

<span data-ttu-id="eb9dc-115">Эта команда представляет задание data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="eb9dc-115">This command submits a Data Lake Analytics job.</span></span>

### <span data-ttu-id="eb9dc-116">Пример 2. Отправка задания с параметрами сценария</span><span class="sxs-lookup"><span data-stu-id="eb9dc-116">Example 2: Submit a job with script parameters</span></span>
```
PS C:\>$parameters = [ordered]@{}
$parameters["Department"] = "Sales"
$parameters["NumRecords"] = 1000
$parameters["StartDateTime"] = (Get-Date).AddDays(-14)
Submit-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32 -ScriptParameter $parameters
```

<span data-ttu-id="eb9dc-117">Параметры сценария U-SQL предварительно заданы над содержимым основного сценария, например: DECLARE @Department string = "Sales"; DECLARE @NumRecords int = 1000; DECLARE @StartDateTime DateTime = new DateTime(2017, 12, 6, 0, 0, 0, 0);</span><span class="sxs-lookup"><span data-stu-id="eb9dc-117">U-SQL script parameters are prepended above the main script contents, e.g.: DECLARE @Department string = "Sales"; DECLARE @NumRecords int = 1000; DECLARE @StartDateTime DateTime = new DateTime(2017, 12, 6, 0, 0, 0, 0);</span></span>

## <span data-ttu-id="eb9dc-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eb9dc-118">PARAMETERS</span></span>

### <span data-ttu-id="eb9dc-119">-Account</span><span class="sxs-lookup"><span data-stu-id="eb9dc-119">-Account</span></span>
<span data-ttu-id="eb9dc-120">Имя учетной записи Data Lake Analytics, под которой будет отправлено задание.</span><span class="sxs-lookup"><span data-stu-id="eb9dc-120">Name of Data Lake Analytics account under which the job will be submitted.</span></span>

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

### <span data-ttu-id="eb9dc-121">-AnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="eb9dc-121">-AnalyticsUnits</span></span>
<span data-ttu-id="eb9dc-122">Аналитические единицы для этого задания.</span><span class="sxs-lookup"><span data-stu-id="eb9dc-122">The analytics units to use for this job.</span></span> <span data-ttu-id="eb9dc-123">Обычно больше аналитических единиц, выделенных для сценария, ускоряют выполнение сценария.</span><span class="sxs-lookup"><span data-stu-id="eb9dc-123">Typically, more analytics units dedicated to a script results in faster script execution time.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: DegreeOfParallelism

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb9dc-124">-CompileMode</span><span class="sxs-lookup"><span data-stu-id="eb9dc-124">-CompileMode</span></span>
<span data-ttu-id="eb9dc-125">Тип компиляции для этого задания.</span><span class="sxs-lookup"><span data-stu-id="eb9dc-125">The type of compilation to be done on this job.</span></span> <span data-ttu-id="eb9dc-126">Допустимые значения</span><span class="sxs-lookup"><span data-stu-id="eb9dc-126">Valid values:</span></span> 
- <span data-ttu-id="eb9dc-127">Семантическая (выполняет только семантические проверки и необходимые проверки вех)</span><span class="sxs-lookup"><span data-stu-id="eb9dc-127">Semantic (Only performs semantic checks and necessary sanity checks)</span></span>
- <span data-ttu-id="eb9dc-128">Полная компиляция</span><span class="sxs-lookup"><span data-stu-id="eb9dc-128">Full (Full compilation)</span></span>
- <span data-ttu-id="eb9dc-129">SingleBox (полная компиляция, выполненная локально)</span><span class="sxs-lookup"><span data-stu-id="eb9dc-129">SingleBox (Full compilation performed locally)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Semantic, Full, SingleBox

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb9dc-130">-CompileOnly</span><span class="sxs-lookup"><span data-stu-id="eb9dc-130">-CompileOnly</span></span>
<span data-ttu-id="eb9dc-131">Указывает на то, что отправка должна построить задание и не выполняться, если для этого установлено истинное.</span><span class="sxs-lookup"><span data-stu-id="eb9dc-131">Indicates that the submission should only build the job and not execute if set to true.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb9dc-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb9dc-132">-DefaultProfile</span></span>
<span data-ttu-id="eb9dc-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="eb9dc-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb9dc-134">-Name</span><span class="sxs-lookup"><span data-stu-id="eb9dc-134">-Name</span></span>
<span data-ttu-id="eb9dc-135">Удобное имя задания, которое нужно отправить.</span><span class="sxs-lookup"><span data-stu-id="eb9dc-135">The friendly name of the job to submit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb9dc-136">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="eb9dc-136">-PipelineId</span></span>
<span data-ttu-id="eb9dc-137">ID that indicates the submission of this job is part of a set of recurring jobs and also associated with a job pipeline.</span><span class="sxs-lookup"><span data-stu-id="eb9dc-137">An ID that indicates the submission of this job is a part of a set of recurring jobs and also associated with a job pipeline.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb9dc-138">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="eb9dc-138">-PipelineName</span></span>
<span data-ttu-id="eb9dc-139">Необязательное удобное имя для конвейера, связанного с этим заданием.</span><span class="sxs-lookup"><span data-stu-id="eb9dc-139">An optional friendly name for the pipeline associated with this job.</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb9dc-140">-PipelineUri</span><span class="sxs-lookup"><span data-stu-id="eb9dc-140">-PipelineUri</span></span>
<span data-ttu-id="eb9dc-141">Необязательный URI, который связывает службу, связанную с этим каналом.</span><span class="sxs-lookup"><span data-stu-id="eb9dc-141">An optional uri that links to the originating service associated with this pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb9dc-142">-Priority</span><span class="sxs-lookup"><span data-stu-id="eb9dc-142">-Priority</span></span>
<span data-ttu-id="eb9dc-143">Приоритет задания.</span><span class="sxs-lookup"><span data-stu-id="eb9dc-143">The priority of the job.</span></span> <span data-ttu-id="eb9dc-144">Если не указано, приоритет — 1000.</span><span class="sxs-lookup"><span data-stu-id="eb9dc-144">If not specified, the priority is 1000.</span></span> <span data-ttu-id="eb9dc-145">Более низкое число означает более высокий приоритет задания.</span><span class="sxs-lookup"><span data-stu-id="eb9dc-145">A lower number indicates a higher job priority.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb9dc-146">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="eb9dc-146">-RecurrenceId</span></span>
<span data-ttu-id="eb9dc-147">An ID that indicates the submission of this job is a part of a set of recurring jobs with the same recurrence ID.</span><span class="sxs-lookup"><span data-stu-id="eb9dc-147">An ID that indicates the submission of this job is a part of a set of recurring jobs with the same recurrence ID.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb9dc-148">-RecurrenceName</span><span class="sxs-lookup"><span data-stu-id="eb9dc-148">-RecurrenceName</span></span>
<span data-ttu-id="eb9dc-149">Необязательное удобное имя для корреляции повторения между заданиями.</span><span class="sxs-lookup"><span data-stu-id="eb9dc-149">An optional friendly name for the recurrence correlation between jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb9dc-150">-RunId</span><span class="sxs-lookup"><span data-stu-id="eb9dc-150">-RunId</span></span>
<span data-ttu-id="eb9dc-151">Идентификатор, который определяет эту итерацию запуска конвейера.</span><span class="sxs-lookup"><span data-stu-id="eb9dc-151">An ID that identifies this specific run iteration of the pipeline.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb9dc-152">-Runtime</span><span class="sxs-lookup"><span data-stu-id="eb9dc-152">-Runtime</span></span>
<span data-ttu-id="eb9dc-153">При желании установите версию времени запуска, используемую для задания.</span><span class="sxs-lookup"><span data-stu-id="eb9dc-153">Optionally set the version of the runtime to use for the job.</span></span> <span data-ttu-id="eb9dc-154">Если это не так, используется стандартное время запуска.</span><span class="sxs-lookup"><span data-stu-id="eb9dc-154">If left unset, the default runtime is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb9dc-155">-Script</span><span class="sxs-lookup"><span data-stu-id="eb9dc-155">-Script</span></span>
<span data-ttu-id="eb9dc-156">Сценарий, который нужно выполнить (в тексте).</span><span class="sxs-lookup"><span data-stu-id="eb9dc-156">Script to execute (written inline).</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJob, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithPipeline
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb9dc-157">-ScriptParameter</span><span class="sxs-lookup"><span data-stu-id="eb9dc-157">-ScriptParameter</span></span>
<span data-ttu-id="eb9dc-158">Параметры сценария для этого задания, в качестве словаря имен параметров (строка) со значениями (любое сочетание byte, sbyte, int, uint (или uint32), long, ulong (или uint64), float, double, decimal, short (или int16), ushort (или uint16), char, string, DateTime, bool, Guid или byte[]).</span><span class="sxs-lookup"><span data-stu-id="eb9dc-158">The script parameters for this job, as a dictionary of parameter names (string) to values (any combination of byte, sbyte, int, uint (or uint32), long, ulong (or uint64), float, double, decimal, short (or int16), ushort (or uint16), char, string, DateTime, bool, Guid, or byte[]).</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb9dc-159">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="eb9dc-159">-ScriptPath</span></span>
<span data-ttu-id="eb9dc-160">Путь к файлу сценария, который нужно отправить.</span><span class="sxs-lookup"><span data-stu-id="eb9dc-160">Path to the script file to submit.</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJobWithScriptPath, SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithScriptPathAndPipeline
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb9dc-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb9dc-161">CommonParameters</span></span>
<span data-ttu-id="eb9dc-162">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb9dc-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb9dc-163">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb9dc-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb9dc-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eb9dc-164">INPUTS</span></span>

### <span data-ttu-id="eb9dc-165">System.String</span><span class="sxs-lookup"><span data-stu-id="eb9dc-165">System.String</span></span>

### <span data-ttu-id="eb9dc-166">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="eb9dc-166">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="eb9dc-167">System.Int32</span><span class="sxs-lookup"><span data-stu-id="eb9dc-167">System.Int32</span></span>

### <span data-ttu-id="eb9dc-168">System.Collections.IDictionary</span><span class="sxs-lookup"><span data-stu-id="eb9dc-168">System.Collections.IDictionary</span></span>

### <span data-ttu-id="eb9dc-169">System.Guid</span><span class="sxs-lookup"><span data-stu-id="eb9dc-169">System.Guid</span></span>

### <span data-ttu-id="eb9dc-170">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="eb9dc-170">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="eb9dc-171">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="eb9dc-171">OUTPUTS</span></span>

### <span data-ttu-id="eb9dc-172">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span><span class="sxs-lookup"><span data-stu-id="eb9dc-172">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="eb9dc-173">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="eb9dc-173">NOTES</span></span>

## <span data-ttu-id="eb9dc-174">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eb9dc-174">RELATED LINKS</span></span>

[<span data-ttu-id="eb9dc-175">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="eb9dc-175">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="eb9dc-176">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="eb9dc-176">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="eb9dc-177">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="eb9dc-177">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)


