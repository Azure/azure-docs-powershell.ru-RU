---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0DB9595A-6C8B-4F3F-A707-2DB41D7C7470
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Submit-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Submit-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: bb0ad536d738facdfe50bc7983517f4505ab4ef2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566740"
---
# <span data-ttu-id="56216-101">Submit-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="56216-101">Submit-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="56216-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="56216-102">SYNOPSIS</span></span>
<span data-ttu-id="56216-103">Отправляет задание.</span><span class="sxs-lookup"><span data-stu-id="56216-103">Submits a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56216-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="56216-104">SYNTAX</span></span>

### <span data-ttu-id="56216-105">Отправка задания с помощью пути сценария для U-SQL</span><span class="sxs-lookup"><span data-stu-id="56216-105">Submit job with script path for U-SQL</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56216-106">Отправка задания на U-SQL</span><span class="sxs-lookup"><span data-stu-id="56216-106">Submit U-SQL Job</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56216-107">Отправка задания с помощью пути сценария для U-SQL с данными reucurrence</span><span class="sxs-lookup"><span data-stu-id="56216-107">Submit job with script path for U-SQL with reucurrence information</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56216-108">Отправка задания из U-SQL с данными о повторении</span><span class="sxs-lookup"><span data-stu-id="56216-108">Submit U-SQL Job with recurrence information</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56216-109">Отправка задания с помощью пути сценария для U-SQL со сведениями о reucurrence и конвейере</span><span class="sxs-lookup"><span data-stu-id="56216-109">Submit job with script path for U-SQL with reucurrence and pipeline information</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="56216-110">Отправка задания в виде "U-SQL" с данными о повторении и конвейере</span><span class="sxs-lookup"><span data-stu-id="56216-110">Submit U-SQL Job with recurrence and pipeline information</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="56216-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="56216-111">DESCRIPTION</span></span>
<span data-ttu-id="56216-112">Командлет **Submit-AzureRmDataLakeAnalyticsJob** отправляет задание Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="56216-112">The **Submit-AzureRmDataLakeAnalyticsJob** cmdlet submits an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="56216-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="56216-113">EXAMPLES</span></span>

### <span data-ttu-id="56216-114">Пример 1: отправка задания</span><span class="sxs-lookup"><span data-stu-id="56216-114">Example 1: Submit a job</span></span>
```
PS C:\>Submit-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -DegreeOfParallelism 32
```

<span data-ttu-id="56216-115">Эта команда отправляет задание Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="56216-115">This command submits a Data Lake Analytics job.</span></span>

## <span data-ttu-id="56216-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="56216-116">PARAMETERS</span></span>

### <span data-ttu-id="56216-117">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="56216-117">-Account</span></span>
<span data-ttu-id="56216-118">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="56216-118">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="56216-119">-CompileMode</span><span class="sxs-lookup"><span data-stu-id="56216-119">-CompileMode</span></span>
<span data-ttu-id="56216-120">Задает режим компиляции задания.</span><span class="sxs-lookup"><span data-stu-id="56216-120">Specifies the compilation mode of the job.</span></span>
<span data-ttu-id="56216-121">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="56216-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="56216-122">Сброса</span><span class="sxs-lookup"><span data-stu-id="56216-122">Semantic</span></span>
- <span data-ttu-id="56216-123">Всех</span><span class="sxs-lookup"><span data-stu-id="56216-123">Full</span></span>
- <span data-ttu-id="56216-124">SingleBox</span><span class="sxs-lookup"><span data-stu-id="56216-124">SingleBox</span></span>

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

### <span data-ttu-id="56216-125">-CompileOnly</span><span class="sxs-lookup"><span data-stu-id="56216-125">-CompileOnly</span></span>
<span data-ttu-id="56216-126">Указывает на то, что этот командлет компилирует задание, не запуская его.</span><span class="sxs-lookup"><span data-stu-id="56216-126">Indicates that this cmdlet compiles the job without running it.</span></span>

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

### <span data-ttu-id="56216-127">-DegreeOfParallelism</span><span class="sxs-lookup"><span data-stu-id="56216-127">-DegreeOfParallelism</span></span>
<span data-ttu-id="56216-128">Задает единицы измерения Data Lake Analytics (DLAU) для задания, которые обозначают максимально допустимый параллелизм задания.</span><span class="sxs-lookup"><span data-stu-id="56216-128">Specifies the Data Lake Analytics Units (DLAU) of the job, which indicates the maximum allowable parallelism of the job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56216-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="56216-129">-Name</span></span>
<span data-ttu-id="56216-130">Указывает имя задания.</span><span class="sxs-lookup"><span data-stu-id="56216-130">Specifies the job name.</span></span>

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

### <span data-ttu-id="56216-131">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="56216-131">-PipelineId</span></span>
<span data-ttu-id="56216-132">Идентификатор, указывающий на то, что отправка задания является частью набора повторяющихся заданий, а также связанных с конвейером заданий.</span><span class="sxs-lookup"><span data-stu-id="56216-132">An ID that indicates the submission of this job is a part of a set of recurring jobs and also associated with a job pipeline.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56216-133">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="56216-133">-PipelineName</span></span>
<span data-ttu-id="56216-134">Необязательное понятное имя для конвейера, связанного с этим заданием.</span><span class="sxs-lookup"><span data-stu-id="56216-134">An optional friendly name for the pipeline associated with this job.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56216-135">-PipelineUri</span><span class="sxs-lookup"><span data-stu-id="56216-135">-PipelineUri</span></span>
<span data-ttu-id="56216-136">Необязательный универсальный код ресурса (URI), который ссылается на службу источника, связанную с этим конвейером.</span><span class="sxs-lookup"><span data-stu-id="56216-136">An optional uri that links to the originating service associated with this pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56216-137">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="56216-137">-Priority</span></span>
<span data-ttu-id="56216-138">Задает приоритет задания.</span><span class="sxs-lookup"><span data-stu-id="56216-138">Specifies the priority of the job.</span></span>
<span data-ttu-id="56216-139">Если значение не указано, то приоритет равен 1000.</span><span class="sxs-lookup"><span data-stu-id="56216-139">If not specified, the priority is 1000.</span></span>
<span data-ttu-id="56216-140">Небольшое число означает более высокий приоритет задания.</span><span class="sxs-lookup"><span data-stu-id="56216-140">A low number indicates a higher job priority.</span></span>

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

### <span data-ttu-id="56216-141">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="56216-141">-RecurrenceId</span></span>
<span data-ttu-id="56216-142">Идентификатор, указывающий на то, что отправка задания является частью набора повторяющихся заданий с одинаковым ИДЕНТИФИКАТОРом повторения.</span><span class="sxs-lookup"><span data-stu-id="56216-142">An ID that indicates the submission of this job is a part of a set of recurring jobs with the same recurrence ID.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Submit job with script path for U-SQL with reucurrence information, Submit U-SQL Job with recurrence information, Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56216-143">-RecurrenceName</span><span class="sxs-lookup"><span data-stu-id="56216-143">-RecurrenceName</span></span>
<span data-ttu-id="56216-144">Необязательное понятное имя для корреляции между заданиями.</span><span class="sxs-lookup"><span data-stu-id="56216-144">An optional friendly name for the recurrence correlation between jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL with reucurrence information, Submit U-SQL Job with recurrence information, Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56216-145">-RunId</span><span class="sxs-lookup"><span data-stu-id="56216-145">-RunId</span></span>
<span data-ttu-id="56216-146">Идентификатор, обозначающий эту конкретную итерацию выполнения конвейера.</span><span class="sxs-lookup"><span data-stu-id="56216-146">An ID that identifies this specific run iteration of the pipeline.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56216-147">-Runtime</span><span class="sxs-lookup"><span data-stu-id="56216-147">-Runtime</span></span>
<span data-ttu-id="56216-148">Указывает версию среды выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="56216-148">Specifies the runtime version of the job.</span></span>

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

### <span data-ttu-id="56216-149">-Сценарий</span><span class="sxs-lookup"><span data-stu-id="56216-149">-Script</span></span>
<span data-ttu-id="56216-150">Определяет содержимое сценария, который необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="56216-150">Specifies the contents of the script to run.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit U-SQL Job, Submit U-SQL Job with recurrence information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56216-151">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="56216-151">-ScriptPath</span></span>
<span data-ttu-id="56216-152">Указывает путь к локальному файлу сценария для запуска.</span><span class="sxs-lookup"><span data-stu-id="56216-152">Specifies the local file path to the script to run.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL, Submit job with script path for U-SQL with reucurrence information, Submit job with script path for U-SQL with reucurrence and pipeline information
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56216-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56216-153">-DefaultProfile</span></span>
<span data-ttu-id="56216-154">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="56216-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56216-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56216-155">CommonParameters</span></span>
<span data-ttu-id="56216-156">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="56216-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56216-157">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56216-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56216-158">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="56216-158">INPUTS</span></span>

### <span data-ttu-id="56216-159">Подстрок</span><span class="sxs-lookup"><span data-stu-id="56216-159">String</span></span>
<span data-ttu-id="56216-160">Параметр "сценарий" принимает значение типа "String" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="56216-160">Parameter 'Script' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="56216-161">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="56216-161">OUTPUTS</span></span>

### <span data-ttu-id="56216-162">JobInformation</span><span class="sxs-lookup"><span data-stu-id="56216-162">JobInformation</span></span>
<span data-ttu-id="56216-163">Начальные сведения о задании для отправленного задания.</span><span class="sxs-lookup"><span data-stu-id="56216-163">The initial job details for the submitted job.</span></span>

## <span data-ttu-id="56216-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="56216-164">NOTES</span></span>

## <span data-ttu-id="56216-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="56216-165">RELATED LINKS</span></span>

[<span data-ttu-id="56216-166">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="56216-166">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="56216-167">Остановить-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="56216-167">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="56216-168">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="56216-168">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


