---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0DB9595A-6C8B-4F3F-A707-2DB41D7C7470
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/submit-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Submit-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Submit-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 2fcd30c523508620d7d7ed20ebce60facc2678a0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077861"
---
# <span data-ttu-id="838e5-101">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="838e5-101">Submit-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="838e5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="838e5-102">SYNOPSIS</span></span>
<span data-ttu-id="838e5-103">Отправляет задание.</span><span class="sxs-lookup"><span data-stu-id="838e5-103">Submits a job.</span></span>

## <span data-ttu-id="838e5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="838e5-104">SYNTAX</span></span>

### <span data-ttu-id="838e5-105">SubmitUSqlJobWithScriptPath</span><span class="sxs-lookup"><span data-stu-id="838e5-105">SubmitUSqlJobWithScriptPath</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="838e5-106">SubmitUSqlJob</span><span class="sxs-lookup"><span data-stu-id="838e5-106">SubmitUSqlJob</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="838e5-107">SubmitUSqlJobWithScriptPathAndRecurrence</span><span class="sxs-lookup"><span data-stu-id="838e5-107">SubmitUSqlJobWithScriptPathAndRecurrence</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="838e5-108">SubmitUSqlJobWithRecurrence</span><span class="sxs-lookup"><span data-stu-id="838e5-108">SubmitUSqlJobWithRecurrence</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="838e5-109">SubmitUSqlJobWithScriptPathAndPipeline</span><span class="sxs-lookup"><span data-stu-id="838e5-109">SubmitUSqlJobWithScriptPathAndPipeline</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="838e5-110">SubmitUSqlJobWithPipeline</span><span class="sxs-lookup"><span data-stu-id="838e5-110">SubmitUSqlJobWithPipeline</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="838e5-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="838e5-111">DESCRIPTION</span></span>
<span data-ttu-id="838e5-112">Командлет **Submit-AzDataLakeAnalyticsJob** отправляет задание Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="838e5-112">The **Submit-AzDataLakeAnalyticsJob** cmdlet submits an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="838e5-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="838e5-113">EXAMPLES</span></span>

### <span data-ttu-id="838e5-114">Пример 1: отправка задания</span><span class="sxs-lookup"><span data-stu-id="838e5-114">Example 1: Submit a job</span></span>
```
PS C:\>Submit-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32
```

<span data-ttu-id="838e5-115">Эта команда отправляет задание Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="838e5-115">This command submits a Data Lake Analytics job.</span></span>

### <span data-ttu-id="838e5-116">Пример 2: отправка задания с параметрами сценария</span><span class="sxs-lookup"><span data-stu-id="838e5-116">Example 2: Submit a job with script parameters</span></span>
```
PS C:\>$parameters = [ordered]@{}
$parameters["Department"] = "Sales"
$parameters["NumRecords"] = 1000
$parameters["StartDateTime"] = (Get-Date).AddDays(-14)
Submit-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32 -ScriptParameter $parameters
```

<span data-ttu-id="838e5-117">Параметры сценария U-SQL добавляются в начале основного содержимого сценария, например: DECLARE @Department String = "Sales"; DECLARE @NumRecords int = 1000; DECLARE @StartDateTime DateTime = New DateTime (2017, 12, 6, 0, 0, 0, 0);</span><span class="sxs-lookup"><span data-stu-id="838e5-117">U-SQL script parameters are prepended above the main script contents, e.g.: DECLARE @Department string = "Sales"; DECLARE @NumRecords int = 1000; DECLARE @StartDateTime DateTime = new DateTime(2017, 12, 6, 0, 0, 0, 0);</span></span>

## <span data-ttu-id="838e5-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="838e5-118">PARAMETERS</span></span>

### <span data-ttu-id="838e5-119">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="838e5-119">-Account</span></span>
<span data-ttu-id="838e5-120">Имя учетной записи Data Lake Analytics, в которой будет отправлено задание.</span><span class="sxs-lookup"><span data-stu-id="838e5-120">Name of Data Lake Analytics account under which the job will be submitted.</span></span>

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

### <span data-ttu-id="838e5-121">-AnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="838e5-121">-AnalyticsUnits</span></span>
<span data-ttu-id="838e5-122">Единицы аналитики, которые нужно использовать для этого задания.</span><span class="sxs-lookup"><span data-stu-id="838e5-122">The analytics units to use for this job.</span></span> <span data-ttu-id="838e5-123">Обычно другие единицы измерения, выделенные для сценария, ускоряют время выполнения сценария.</span><span class="sxs-lookup"><span data-stu-id="838e5-123">Typically, more analytics units dedicated to a script results in faster script execution time.</span></span>

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

### <span data-ttu-id="838e5-124">-CompileMode</span><span class="sxs-lookup"><span data-stu-id="838e5-124">-CompileMode</span></span>
<span data-ttu-id="838e5-125">Тип компиляции, которая должна быть выполнена для этого задания.</span><span class="sxs-lookup"><span data-stu-id="838e5-125">The type of compilation to be done on this job.</span></span> <span data-ttu-id="838e5-126">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="838e5-126">Valid values:</span></span> 
- <span data-ttu-id="838e5-127">Семантика (выполняются только семантические проверки и необходимые проверки работоспособности)</span><span class="sxs-lookup"><span data-stu-id="838e5-127">Semantic (Only performs semantic checks and necessary sanity checks)</span></span>
- <span data-ttu-id="838e5-128">Полная (полная компиляция)</span><span class="sxs-lookup"><span data-stu-id="838e5-128">Full (Full compilation)</span></span>
- <span data-ttu-id="838e5-129">SingleBox (полная компиляция выполнена локально)</span><span class="sxs-lookup"><span data-stu-id="838e5-129">SingleBox (Full compilation performed locally)</span></span>

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

### <span data-ttu-id="838e5-130">-CompileOnly</span><span class="sxs-lookup"><span data-stu-id="838e5-130">-CompileOnly</span></span>
<span data-ttu-id="838e5-131">Указывает на то, что при отправке должна выполняться только сборка задания, но не выполнение, если установлено значение true.</span><span class="sxs-lookup"><span data-stu-id="838e5-131">Indicates that the submission should only build the job and not execute if set to true.</span></span>

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

### <span data-ttu-id="838e5-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="838e5-132">-DefaultProfile</span></span>
<span data-ttu-id="838e5-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="838e5-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="838e5-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="838e5-134">-Name</span></span>
<span data-ttu-id="838e5-135">Понятное имя задания для отправки.</span><span class="sxs-lookup"><span data-stu-id="838e5-135">The friendly name of the job to submit.</span></span>

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

### <span data-ttu-id="838e5-136">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="838e5-136">-PipelineId</span></span>
<span data-ttu-id="838e5-137">Идентификатор, указывающий на то, что отправка задания является частью набора повторяющихся заданий, а также связанных с конвейером заданий.</span><span class="sxs-lookup"><span data-stu-id="838e5-137">An ID that indicates the submission of this job is a part of a set of recurring jobs and also associated with a job pipeline.</span></span>

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

### <span data-ttu-id="838e5-138">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="838e5-138">-PipelineName</span></span>
<span data-ttu-id="838e5-139">Необязательное понятное имя для конвейера, связанного с этим заданием.</span><span class="sxs-lookup"><span data-stu-id="838e5-139">An optional friendly name for the pipeline associated with this job.</span></span>

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

### <span data-ttu-id="838e5-140">-PipelineUri</span><span class="sxs-lookup"><span data-stu-id="838e5-140">-PipelineUri</span></span>
<span data-ttu-id="838e5-141">Необязательный универсальный код ресурса (URI), который ссылается на службу источника, связанную с этим конвейером.</span><span class="sxs-lookup"><span data-stu-id="838e5-141">An optional uri that links to the originating service associated with this pipeline.</span></span>

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

### <span data-ttu-id="838e5-142">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="838e5-142">-Priority</span></span>
<span data-ttu-id="838e5-143">Приоритет задания.</span><span class="sxs-lookup"><span data-stu-id="838e5-143">The priority of the job.</span></span> <span data-ttu-id="838e5-144">Если значение не указано, то приоритет равен 1000.</span><span class="sxs-lookup"><span data-stu-id="838e5-144">If not specified, the priority is 1000.</span></span> <span data-ttu-id="838e5-145">Меньшее число означает более высокий приоритет задания.</span><span class="sxs-lookup"><span data-stu-id="838e5-145">A lower number indicates a higher job priority.</span></span>

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

### <span data-ttu-id="838e5-146">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="838e5-146">-RecurrenceId</span></span>
<span data-ttu-id="838e5-147">Идентификатор, указывающий на то, что отправка задания является частью набора повторяющихся заданий с одинаковым ИДЕНТИФИКАТОРом повторения.</span><span class="sxs-lookup"><span data-stu-id="838e5-147">An ID that indicates the submission of this job is a part of a set of recurring jobs with the same recurrence ID.</span></span>

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

### <span data-ttu-id="838e5-148">-RecurrenceName</span><span class="sxs-lookup"><span data-stu-id="838e5-148">-RecurrenceName</span></span>
<span data-ttu-id="838e5-149">Необязательное понятное имя для корреляции между заданиями.</span><span class="sxs-lookup"><span data-stu-id="838e5-149">An optional friendly name for the recurrence correlation between jobs.</span></span>

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

### <span data-ttu-id="838e5-150">-RunId</span><span class="sxs-lookup"><span data-stu-id="838e5-150">-RunId</span></span>
<span data-ttu-id="838e5-151">Идентификатор, обозначающий эту конкретную итерацию выполнения конвейера.</span><span class="sxs-lookup"><span data-stu-id="838e5-151">An ID that identifies this specific run iteration of the pipeline.</span></span>

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

### <span data-ttu-id="838e5-152">-Runtime</span><span class="sxs-lookup"><span data-stu-id="838e5-152">-Runtime</span></span>
<span data-ttu-id="838e5-153">При необходимости задайте для задания версию среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="838e5-153">Optionally set the version of the runtime to use for the job.</span></span> <span data-ttu-id="838e5-154">Если не указано, используется среда выполнения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="838e5-154">If left unset, the default runtime is used.</span></span>

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

### <span data-ttu-id="838e5-155">-Сценарий</span><span class="sxs-lookup"><span data-stu-id="838e5-155">-Script</span></span>
<span data-ttu-id="838e5-156">Выполняемый сценарий (рукописный текст).</span><span class="sxs-lookup"><span data-stu-id="838e5-156">Script to execute (written inline).</span></span>

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

### <span data-ttu-id="838e5-157">-ScriptParameter</span><span class="sxs-lookup"><span data-stu-id="838e5-157">-ScriptParameter</span></span>
<span data-ttu-id="838e5-158">Параметры сценария для этого задания в виде словаря имен параметров (строковых значений) к значениям (любое сочетание типа Byte, SByte, int, uint (или UInt32), Long, ulong (или UInt64), float, Double, Decimal, short (или Int16), char (или UInt16), "ushort", "число"</span><span class="sxs-lookup"><span data-stu-id="838e5-158">The script parameters for this job, as a dictionary of parameter names (string) to values (any combination of byte, sbyte, int, uint (or uint32), long, ulong (or uint64), float, double, decimal, short (or int16), ushort (or uint16), char, string, DateTime, bool, Guid, or byte[]).</span></span>

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

### <span data-ttu-id="838e5-159">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="838e5-159">-ScriptPath</span></span>
<span data-ttu-id="838e5-160">Путь к файлу сценария, который нужно отправить.</span><span class="sxs-lookup"><span data-stu-id="838e5-160">Path to the script file to submit.</span></span>

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

### <span data-ttu-id="838e5-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="838e5-161">CommonParameters</span></span>
<span data-ttu-id="838e5-162">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="838e5-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="838e5-163">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="838e5-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="838e5-164">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="838e5-164">INPUTS</span></span>

### <span data-ttu-id="838e5-165">System. String</span><span class="sxs-lookup"><span data-stu-id="838e5-165">System.String</span></span>

### <span data-ttu-id="838e5-166">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="838e5-166">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="838e5-167">System. Int32</span><span class="sxs-lookup"><span data-stu-id="838e5-167">System.Int32</span></span>

### <span data-ttu-id="838e5-168">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="838e5-168">System.Collections.IDictionary</span></span>

### <span data-ttu-id="838e5-169">System. GUID</span><span class="sxs-lookup"><span data-stu-id="838e5-169">System.Guid</span></span>

### <span data-ttu-id="838e5-170">System. Nullable "1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="838e5-170">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="838e5-171">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="838e5-171">OUTPUTS</span></span>

### <span data-ttu-id="838e5-172">Microsoft. Azure. Management. данных Lake. Analytics. Models. JobInformation</span><span class="sxs-lookup"><span data-stu-id="838e5-172">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="838e5-173">Пуск</span><span class="sxs-lookup"><span data-stu-id="838e5-173">NOTES</span></span>

## <span data-ttu-id="838e5-174">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="838e5-174">RELATED LINKS</span></span>

[<span data-ttu-id="838e5-175">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="838e5-175">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="838e5-176">Остановить-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="838e5-176">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="838e5-177">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="838e5-177">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)


