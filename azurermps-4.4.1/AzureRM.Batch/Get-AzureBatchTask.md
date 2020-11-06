---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 4B5FE41A-090B-4859-B021-05CF0A8B7882
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTask.md
ms.openlocfilehash: fb01af87d28323e3e25c46868f94e892b835afc7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568093"
---
# <span data-ttu-id="10fc3-101">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="10fc3-101">Get-AzureBatchTask</span></span>

## <span data-ttu-id="10fc3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="10fc3-102">SYNOPSIS</span></span>
<span data-ttu-id="10fc3-103">Возвращает пакетные задачи для задания.</span><span class="sxs-lookup"><span data-stu-id="10fc3-103">Gets the Batch tasks for a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10fc3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="10fc3-104">SYNTAX</span></span>

### <span data-ttu-id="10fc3-105">ODataFilter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="10fc3-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchTask [-JobId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="10fc3-106">Номер</span><span class="sxs-lookup"><span data-stu-id="10fc3-106">Id</span></span>
```
Get-AzureBatchTask [-JobId] <String> [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10fc3-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="10fc3-107">ParentObject</span></span>
```
Get-AzureBatchTask [[-Job] <PSCloudJob>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="10fc3-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="10fc3-108">DESCRIPTION</span></span>
<span data-ttu-id="10fc3-109">Командлет **Get-AzureBatchTask** получает пакетные задачи Azure для пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="10fc3-109">The **Get-AzureBatchTask** cmdlet gets Azure Batch tasks for a Batch job.</span></span>
<span data-ttu-id="10fc3-110">Укажите задание с помощью параметра *JOBID* или параметра *задания* .</span><span class="sxs-lookup"><span data-stu-id="10fc3-110">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="10fc3-111">Чтобы получить одну задачу, укажите параметр *ID* .</span><span class="sxs-lookup"><span data-stu-id="10fc3-111">To get a single task, specify the *Id* parameter.</span></span>
<span data-ttu-id="10fc3-112">Вы можете указать параметр *Filter* , чтобы получить задачи, соответствующие фильтру Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="10fc3-112">You can specify the *Filter* parameter to get the tasks that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="10fc3-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="10fc3-113">EXAMPLES</span></span>

### <span data-ttu-id="10fc3-114">Пример 1: получение задачи по ИДЕНТИФИКАТОРу</span><span class="sxs-lookup"><span data-stu-id="10fc3-114">Example 1: Get a task by ID</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job01" -Id "Task03" -BatchContext $Context
AffinityInformation         : 
CommandLine                 : cmd /c dir /s
ComputeNodeInformation      : Microsoft.Azure.Commands.Batch.Models.PSComputeNodeInformation
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
CreationTime                : 7/25/2015 11:24:52 PM
DisplayName                 : 
EnvironmentSettings         : 
ETag                        : 0x8D295483E08BD9D
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSTaskExecutionInformation
Id                          : Task03
LastModified                : 7/25/2015 11:24:52 PM
PreviousState               : Running
PreviousStateTransitionTime : 7/25/2015 11:24:59 PM
ResourceFiles               : 
RunElevated                 : False
State                       : Completed
StateTransitionTime         : 7/25/2015 11:24:59 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job01/tasks/Task03
```

<span data-ttu-id="10fc3-115">Эта команда получает задачу с ИДЕНТИФИКАТОРом Task03 в разделе задания Job01.</span><span class="sxs-lookup"><span data-stu-id="10fc3-115">This command gets the task with ID Task03 under job Job01.</span></span>
<span data-ttu-id="10fc3-116">Используйте командлет Get-AzureRmBatchAccountKeys для присвоения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="10fc3-116">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="10fc3-117">Пример 2: получение всех завершенных задач из указанного задания</span><span class="sxs-lookup"><span data-stu-id="10fc3-117">Example 2: Get all completed tasks from a specified job</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job02" -Filter "state eq 'completed'" -BatchContext $Context
AffinityInformation         : 
CommandLine                 : cmd /c dir /s
ComputeNodeInformation      : Microsoft.Azure.Commands.Batch.Models.PSComputeNodeInformation
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
CreationTime                : 3/24/2015 10:21:51 PM
EnvironmentSettings         : 
ETag                        : 0x8D295483E08BD9D
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSTaskExecutionInformation
Id                          : Task17
LastModified                : 3/24/2015 10:21:51 PM
PreviousState               : Running
PreviousStateTransitionTime : 3/24/2015 10:22:00 PM
ResourceFiles               : 
RunElevated                 : False
State                       : Completed
StateTransitionTime         : 3/24/2015 10:22:00 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job02/tasks/Task17

AffinityInformation         : 
CommandLine                 : cmd /c echo hello > newFile.txt
ComputeNodeInformation      : Microsoft.Azure.Commands.Batch.Models.PSComputeNodeInformation
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
CreationTime                : 3/24/2015 10:21:51 PM
EnvironmentSettings         : 
ETag                        : 0x8D295483E08BD9D
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSTaskExecutionInformation
Id                          : Task27
LastModified                : 3/24/2015 10:23:35 PM
PreviousState               : Running
PreviousStateTransitionTime : 3/24/2015 10:23:37 PM
ResourceFiles               : 
RunElevated                 : True
State                       : Completed
StateTransitionTime         : 3/24/2015 10:23:37 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job02/tasks/Task27
```

<span data-ttu-id="10fc3-118">Эта команда получает завершенные задачи из задания с ИДЕНТИФИКАТОРом Job02.</span><span class="sxs-lookup"><span data-stu-id="10fc3-118">This command gets the completed tasks from the job that has the ID Job02.</span></span>

## <span data-ttu-id="10fc3-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="10fc3-119">PARAMETERS</span></span>

### <span data-ttu-id="10fc3-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="10fc3-120">-BatchContext</span></span>
<span data-ttu-id="10fc3-121">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="10fc3-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="10fc3-122">Чтобы получить объект **BatchAccountContext** , содержащий клавиши доступа для вашей подписки, используйте командлет Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="10fc3-122">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10fc3-123">-Expand</span><span class="sxs-lookup"><span data-stu-id="10fc3-123">-Expand</span></span>
<span data-ttu-id="10fc3-124">Задает предложение развертывания OData.</span><span class="sxs-lookup"><span data-stu-id="10fc3-124">Specifies an OData expand clause.</span></span>
<span data-ttu-id="10fc3-125">Укажите значение этого параметра, чтобы получить связанные сущности основной сущности.</span><span class="sxs-lookup"><span data-stu-id="10fc3-125">Specify a value for this parameter to get associated entities of the main entity to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10fc3-126">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="10fc3-126">-Filter</span></span>
<span data-ttu-id="10fc3-127">Задает предложение фильтра OData для задач.</span><span class="sxs-lookup"><span data-stu-id="10fc3-127">Specifies an OData filter clause for tasks.</span></span>
<span data-ttu-id="10fc3-128">Если фильтр не указан, этот командлет возвращает все задачи для учетной записи или задания пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="10fc3-128">If you do not specify a filter, this cmdlet returns all tasks for the Batch account or job.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter, ParentObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10fc3-129">-ID</span><span class="sxs-lookup"><span data-stu-id="10fc3-129">-Id</span></span>
<span data-ttu-id="10fc3-130">Указывает идентификатор задачи, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="10fc3-130">Specifies the ID of the task that this cmdlet gets.</span></span>
<span data-ttu-id="10fc3-131">Подстановочные знаки указывать нельзя.</span><span class="sxs-lookup"><span data-stu-id="10fc3-131">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10fc3-132">-Job</span><span class="sxs-lookup"><span data-stu-id="10fc3-132">-Job</span></span>
<span data-ttu-id="10fc3-133">Указывает задание, содержащее задачи, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="10fc3-133">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="10fc3-134">Чтобы получить объект **PSCloudJob** , используйте командлет Get-AzureBatchJob.</span><span class="sxs-lookup"><span data-stu-id="10fc3-134">To obtain a **PSCloudJob** object, use the Get-AzureBatchJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: ParentObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10fc3-135">-JobId</span><span class="sxs-lookup"><span data-stu-id="10fc3-135">-JobId</span></span>
<span data-ttu-id="10fc3-136">Указывает идентификатор задания, содержащего задачи, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="10fc3-136">Specifies the ID of the job that contains the tasks that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter, Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10fc3-137">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="10fc3-137">-MaxCount</span></span>
<span data-ttu-id="10fc3-138">Задает максимальное количество возвращаемых задач.</span><span class="sxs-lookup"><span data-stu-id="10fc3-138">Specifies the maximum number of tasks to return.</span></span>
<span data-ttu-id="10fc3-139">Если вы задаете нулевое значение (0) или меньше, в командлете не используется верхний предел.</span><span class="sxs-lookup"><span data-stu-id="10fc3-139">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="10fc3-140">Значение по умолчанию — 1000.</span><span class="sxs-lookup"><span data-stu-id="10fc3-140">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter, ParentObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10fc3-141">-SELECT</span><span class="sxs-lookup"><span data-stu-id="10fc3-141">-Select</span></span>
<span data-ttu-id="10fc3-142">Задает предложение SELECT OData.</span><span class="sxs-lookup"><span data-stu-id="10fc3-142">Specifies an OData select clause.</span></span>
<span data-ttu-id="10fc3-143">Укажите значение этого параметра, чтобы получить конкретные свойства, а не все свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="10fc3-143">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10fc3-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10fc3-144">-DefaultProfile</span></span>
<span data-ttu-id="10fc3-145">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="10fc3-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10fc3-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10fc3-146">CommonParameters</span></span>
<span data-ttu-id="10fc3-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="10fc3-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10fc3-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10fc3-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10fc3-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="10fc3-149">INPUTS</span></span>

### <span data-ttu-id="10fc3-150">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="10fc3-150">BatchAccountContext</span></span>
<span data-ttu-id="10fc3-151">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="10fc3-151">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="10fc3-152">PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="10fc3-152">PSCloudJob</span></span>
<span data-ttu-id="10fc3-153">Параметр "задание" принимает значение типа "PSCloudJob" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="10fc3-153">Parameter 'Job' accepts value of type 'PSCloudJob' from the pipeline</span></span>

## <span data-ttu-id="10fc3-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="10fc3-154">OUTPUTS</span></span>

### <span data-ttu-id="10fc3-155">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="10fc3-155">PSCloudTask</span></span>

## <span data-ttu-id="10fc3-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="10fc3-156">NOTES</span></span>

## <span data-ttu-id="10fc3-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="10fc3-157">RELATED LINKS</span></span>

[<span data-ttu-id="10fc3-158">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="10fc3-158">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="10fc3-159">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="10fc3-159">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="10fc3-160">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="10fc3-160">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="10fc3-161">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="10fc3-161">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="10fc3-162">Остановить-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="10fc3-162">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="10fc3-163">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="10fc3-163">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


