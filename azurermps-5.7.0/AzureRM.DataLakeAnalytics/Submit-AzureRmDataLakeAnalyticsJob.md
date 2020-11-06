---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0DB9595A-6C8B-4F3F-A707-2DB41D7C7470
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/submit-azurermdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Submit-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Submit-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: fc09560bca0d825cc65d8a4f964119cd50898190
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559092"
---
# <span data-ttu-id="a21ef-101">Submit-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a21ef-101">Submit-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="a21ef-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a21ef-102">SYNOPSIS</span></span>
<span data-ttu-id="a21ef-103">Отправляет задание.</span><span class="sxs-lookup"><span data-stu-id="a21ef-103">Submits a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a21ef-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a21ef-104">SYNTAX</span></span>

### <span data-ttu-id="a21ef-105">SubmitUSqlJobWithScriptPath</span><span class="sxs-lookup"><span data-stu-id="a21ef-105">SubmitUSqlJobWithScriptPath</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a21ef-106">SubmitUSqlJob</span><span class="sxs-lookup"><span data-stu-id="a21ef-106">SubmitUSqlJob</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a21ef-107">SubmitUSqlJobWithScriptPathAndRecurrence</span><span class="sxs-lookup"><span data-stu-id="a21ef-107">SubmitUSqlJobWithScriptPathAndRecurrence</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a21ef-108">SubmitUSqlJobWithRecurrence</span><span class="sxs-lookup"><span data-stu-id="a21ef-108">SubmitUSqlJobWithRecurrence</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a21ef-109">SubmitUSqlJobWithScriptPathAndPipeline</span><span class="sxs-lookup"><span data-stu-id="a21ef-109">SubmitUSqlJobWithScriptPathAndPipeline</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 -PipelineId <Guid> [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a21ef-110">SubmitUSqlJobWithPipeline</span><span class="sxs-lookup"><span data-stu-id="a21ef-110">SubmitUSqlJobWithPipeline</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 -PipelineId <Guid> [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a21ef-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a21ef-111">DESCRIPTION</span></span>
<span data-ttu-id="a21ef-112">Командлет **Submit-AzureRmDataLakeAnalyticsJob** отправляет задание Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="a21ef-112">The **Submit-AzureRmDataLakeAnalyticsJob** cmdlet submits an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="a21ef-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a21ef-113">EXAMPLES</span></span>

### <span data-ttu-id="a21ef-114">Пример 1: отправка задания</span><span class="sxs-lookup"><span data-stu-id="a21ef-114">Example 1: Submit a job</span></span>
```
PS C:\>Submit-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32
```

<span data-ttu-id="a21ef-115">Эта команда отправляет задание Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="a21ef-115">This command submits a Data Lake Analytics job.</span></span>

### <span data-ttu-id="a21ef-116">Пример 2: отправка задания с параметрами сценария</span><span class="sxs-lookup"><span data-stu-id="a21ef-116">Example 2: Submit a job with script parameters</span></span>
```
PS C:\>$parameters = [ordered]@{}
$parameters["Department"] = "Sales"
$parameters["NumRecords"] = 1000
$parameters["StartDateTime"] = (Get-Date).AddDays(-14)
Submit-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32 -ScriptParameter $parameters
```

<span data-ttu-id="a21ef-117">Параметры сценария U-SQL добавляются в начале основного содержимого сценария, например:</span><span class="sxs-lookup"><span data-stu-id="a21ef-117">U-SQL script parameters are prepended above the main script contents, e.g.:</span></span>

<span data-ttu-id="a21ef-118">DECLARE @Department String = "Sales"; DECLARE @NumRecords int = 1000; DECLARE @StartDateTime DateTime = New DateTime (2017, 12, 6, 0, 0, 0, 0);</span><span class="sxs-lookup"><span data-stu-id="a21ef-118">DECLARE @Department string = "Sales"; DECLARE @NumRecords int = 1000; DECLARE @StartDateTime DateTime = new DateTime(2017, 12, 6, 0, 0, 0, 0);</span></span>

## <span data-ttu-id="a21ef-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a21ef-119">PARAMETERS</span></span>

### <span data-ttu-id="a21ef-120">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="a21ef-120">-Account</span></span>
<span data-ttu-id="a21ef-121">Имя учетной записи Data Lake Analytics, в которой будет отправлено задание.</span><span class="sxs-lookup"><span data-stu-id="a21ef-121">Name of Data Lake Analytics account under which the job will be submitted.</span></span>

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

### <span data-ttu-id="a21ef-122">-CompileMode</span><span class="sxs-lookup"><span data-stu-id="a21ef-122">-CompileMode</span></span>
<span data-ttu-id="a21ef-123">Тип компиляции, которая должна быть выполнена для этого задания.</span><span class="sxs-lookup"><span data-stu-id="a21ef-123">The type of compilation to be done on this job.</span></span> <span data-ttu-id="a21ef-124">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="a21ef-124">Valid values:</span></span> 

- <span data-ttu-id="a21ef-125">Семантика (выполняются только семантические проверки и необходимые проверки работоспособности)</span><span class="sxs-lookup"><span data-stu-id="a21ef-125">Semantic (Only performs semantic checks and necessary sanity checks)</span></span>
- <span data-ttu-id="a21ef-126">Полная (полная компиляция)</span><span class="sxs-lookup"><span data-stu-id="a21ef-126">Full (Full compilation)</span></span>
- <span data-ttu-id="a21ef-127">SingleBox (полная компиляция выполнена локально)</span><span class="sxs-lookup"><span data-stu-id="a21ef-127">SingleBox (Full compilation performed locally)</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Semantic, Full, SingleBox

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a21ef-128">-CompileOnly</span><span class="sxs-lookup"><span data-stu-id="a21ef-128">-CompileOnly</span></span>
<span data-ttu-id="a21ef-129">Указывает на то, что при отправке должна выполняться только сборка задания, но не выполнение, если установлено значение true.</span><span class="sxs-lookup"><span data-stu-id="a21ef-129">Indicates that the submission should only build the job and not execute if set to true.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a21ef-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a21ef-130">-DefaultProfile</span></span>
<span data-ttu-id="a21ef-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a21ef-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a21ef-132">-AnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="a21ef-132">-AnalyticsUnits</span></span>
<span data-ttu-id="a21ef-133">Единицы аналитики, которые нужно использовать для этого задания.</span><span class="sxs-lookup"><span data-stu-id="a21ef-133">The analytics units to use for this job.</span></span> <span data-ttu-id="a21ef-134">Обычно другие единицы измерения, выделенные для сценария, ускоряют время выполнения сценария.</span><span class="sxs-lookup"><span data-stu-id="a21ef-134">Typically, more analytics units dedicated to a script results in faster script execution time.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: DegreeOfParallelism

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a21ef-135">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a21ef-135">-Name</span></span>
<span data-ttu-id="a21ef-136">Понятное имя задания для отправки.</span><span class="sxs-lookup"><span data-stu-id="a21ef-136">The friendly name of the job to submit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a21ef-137">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="a21ef-137">-PipelineId</span></span>
<span data-ttu-id="a21ef-138">Идентификатор, указывающий на то, что отправка задания является частью набора повторяющихся заданий, а также связанных с конвейером заданий.</span><span class="sxs-lookup"><span data-stu-id="a21ef-138">An ID that indicates the submission of this job is a part of a set of recurring jobs and also associated with a job pipeline.</span></span>

```yaml
Type: Guid
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a21ef-139">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="a21ef-139">-PipelineName</span></span>
<span data-ttu-id="a21ef-140">Необязательное понятное имя для конвейера, связанного с этим заданием.</span><span class="sxs-lookup"><span data-stu-id="a21ef-140">An optional friendly name for the pipeline associated with this job.</span></span>

```yaml
Type: String
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a21ef-141">-PipelineUri</span><span class="sxs-lookup"><span data-stu-id="a21ef-141">-PipelineUri</span></span>
<span data-ttu-id="a21ef-142">Необязательный универсальный код ресурса (URI), который ссылается на службу источника, связанную с этим конвейером.</span><span class="sxs-lookup"><span data-stu-id="a21ef-142">An optional uri that links to the originating service associated with this pipeline.</span></span>

```yaml
Type: String
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a21ef-143">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="a21ef-143">-Priority</span></span>
<span data-ttu-id="a21ef-144">Приоритет задания.</span><span class="sxs-lookup"><span data-stu-id="a21ef-144">The priority of the job.</span></span> <span data-ttu-id="a21ef-145">Если значение не указано, то приоритет равен 1000.</span><span class="sxs-lookup"><span data-stu-id="a21ef-145">If not specified, the priority is 1000.</span></span> <span data-ttu-id="a21ef-146">Меньшее число означает более высокий приоритет задания.</span><span class="sxs-lookup"><span data-stu-id="a21ef-146">A lower number indicates a higher job priority.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a21ef-147">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="a21ef-147">-RecurrenceId</span></span>
<span data-ttu-id="a21ef-148">Идентификатор, указывающий на то, что отправка задания является частью набора повторяющихся заданий с одинаковым ИДЕНТИФИКАТОРом повторения.</span><span class="sxs-lookup"><span data-stu-id="a21ef-148">An ID that indicates the submission of this job is a part of a set of recurring jobs with the same recurrence ID.</span></span>

```yaml
Type: Guid
Parameter Sets: SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a21ef-149">-RecurrenceName</span><span class="sxs-lookup"><span data-stu-id="a21ef-149">-RecurrenceName</span></span>
<span data-ttu-id="a21ef-150">Необязательное понятное имя для корреляции между заданиями.</span><span class="sxs-lookup"><span data-stu-id="a21ef-150">An optional friendly name for the recurrence correlation between jobs.</span></span>

```yaml
Type: String
Parameter Sets: SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a21ef-151">-RunId</span><span class="sxs-lookup"><span data-stu-id="a21ef-151">-RunId</span></span>
<span data-ttu-id="a21ef-152">Идентификатор, обозначающий эту конкретную итерацию выполнения конвейера.</span><span class="sxs-lookup"><span data-stu-id="a21ef-152">An ID that identifies this specific run iteration of the pipeline.</span></span>

```yaml
Type: Guid
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a21ef-153">-Runtime</span><span class="sxs-lookup"><span data-stu-id="a21ef-153">-Runtime</span></span>
<span data-ttu-id="a21ef-154">При необходимости задайте для задания версию среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="a21ef-154">Optionally set the version of the runtime to use for the job.</span></span> <span data-ttu-id="a21ef-155">Если не указано, используется среда выполнения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a21ef-155">If left unset, the default runtime is used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a21ef-156">-Сценарий</span><span class="sxs-lookup"><span data-stu-id="a21ef-156">-Script</span></span>
<span data-ttu-id="a21ef-157">Выполняемый сценарий (рукописный текст).</span><span class="sxs-lookup"><span data-stu-id="a21ef-157">Script to execute (written inline).</span></span>

```yaml
Type: String
Parameter Sets: SubmitUSqlJob, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithPipeline
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a21ef-158">-ScriptParameter</span><span class="sxs-lookup"><span data-stu-id="a21ef-158">-ScriptParameter</span></span>
<span data-ttu-id="a21ef-159">Параметры сценария для этого задания в виде словаря имен параметров (строковых значений) к значениям (любое сочетание типа Byte, SByte, int, uint (или UInt32), Long, ulong (или UInt64), float, Double, Decimal, short (или Int16), char (или UInt16), "ushort", "число"</span><span class="sxs-lookup"><span data-stu-id="a21ef-159">The script parameters for this job, as a dictionary of parameter names (string) to values (any combination of byte, sbyte, int, uint (or uint32), long, ulong (or uint64), float, double, decimal, short (or int16), ushort (or uint16), char, string, DateTime, bool, Guid, or byte[]).</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a21ef-160">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="a21ef-160">-ScriptPath</span></span>
<span data-ttu-id="a21ef-161">Путь к файлу сценария, который нужно отправить.</span><span class="sxs-lookup"><span data-stu-id="a21ef-161">Path to the script file to submit.</span></span>

```yaml
Type: String
Parameter Sets: SubmitUSqlJobWithScriptPath, SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithScriptPathAndPipeline
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a21ef-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a21ef-162">CommonParameters</span></span>
<span data-ttu-id="a21ef-163">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a21ef-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a21ef-164">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a21ef-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a21ef-165">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a21ef-165">INPUTS</span></span>

### <span data-ttu-id="a21ef-166">Подстрок</span><span class="sxs-lookup"><span data-stu-id="a21ef-166">String</span></span>
<span data-ttu-id="a21ef-167">Параметр "сценарий" принимает значение типа "String" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="a21ef-167">Parameter 'Script' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="a21ef-168">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a21ef-168">OUTPUTS</span></span>

### <span data-ttu-id="a21ef-169">JobInformation</span><span class="sxs-lookup"><span data-stu-id="a21ef-169">JobInformation</span></span>
<span data-ttu-id="a21ef-170">Начальные сведения о задании для отправленного задания.</span><span class="sxs-lookup"><span data-stu-id="a21ef-170">The initial job details for the submitted job.</span></span>

## <span data-ttu-id="a21ef-171">Пуск</span><span class="sxs-lookup"><span data-stu-id="a21ef-171">NOTES</span></span>

## <span data-ttu-id="a21ef-172">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a21ef-172">RELATED LINKS</span></span>

[<span data-ttu-id="a21ef-173">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a21ef-173">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="a21ef-174">Остановить-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a21ef-174">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="a21ef-175">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a21ef-175">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


