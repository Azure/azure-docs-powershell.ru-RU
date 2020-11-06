---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 8BF49C4D-E7CD-4FD0-AFAC-9856239D24EC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJob.md
ms.openlocfilehash: c2aa673b9cd0f8cccc3f1a8721313f5a3236270d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565274"
---
# <span data-ttu-id="fb3a2-101">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="fb3a2-101">Get-AzureBatchJob</span></span>

## <span data-ttu-id="fb3a2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fb3a2-102">SYNOPSIS</span></span>
<span data-ttu-id="fb3a2-103">Возвращает пакетные задания для учетной записи пакетной службы или расписания задания.</span><span class="sxs-lookup"><span data-stu-id="fb3a2-103">Gets Batch jobs for a Batch account or job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb3a2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fb3a2-104">SYNTAX</span></span>

### <span data-ttu-id="fb3a2-105">ODataFilter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fb3a2-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchJob [-JobScheduleId <String>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fb3a2-106">Номер</span><span class="sxs-lookup"><span data-stu-id="fb3a2-106">Id</span></span>
```
Get-AzureBatchJob [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb3a2-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="fb3a2-107">ParentObject</span></span>
```
Get-AzureBatchJob [[-JobSchedule] <PSCloudJobSchedule>] [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb3a2-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb3a2-108">DESCRIPTION</span></span>
<span data-ttu-id="fb3a2-109">Командлет **Get-AzureBatchJob** получает пакетные задания Azure для учетной записи пакетной службы, указанной в параметре *BatchAccountContext* .</span><span class="sxs-lookup"><span data-stu-id="fb3a2-109">The **Get-AzureBatchJob** cmdlet gets the Azure Batch jobs for the Batch account specified by the *BatchAccountContext* parameter.</span></span>
<span data-ttu-id="fb3a2-110">Вы можете использовать параметр *ID* для получения одного задания.</span><span class="sxs-lookup"><span data-stu-id="fb3a2-110">You can use the *Id* parameter to get a single job.</span></span>
<span data-ttu-id="fb3a2-111">С помощью параметра *Filter* можно получить задания, соответствующие фильтру Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="fb3a2-111">You can use the *Filter* parameter to get the jobs that match an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="fb3a2-112">Если вы задаете идентификатор расписания задания или экземпляр **PSCloudJobSchedule** , этот командлет возвращает только задания для этого расписания задания.</span><span class="sxs-lookup"><span data-stu-id="fb3a2-112">If you supply a job schedule ID or **PSCloudJobSchedule** instance, this cmdlet returns only the jobs for that job schedule.</span></span>

## <span data-ttu-id="fb3a2-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fb3a2-113">EXAMPLES</span></span>

### <span data-ttu-id="fb3a2-114">Пример 1: получение пакетного задания по ИДЕНТИФИКАТОРу</span><span class="sxs-lookup"><span data-stu-id="fb3a2-114">Example 1: Get a Batch job by ID</span></span>
```
PS C:\>Get-AzureBatchJob -Id "Job01" -BatchContext $Context
CommonEnvironmentSettings   : 
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
CreationTime                : 7/25/2015 9:12:07 PM
DisplayName                 : 
ETag                        : 0x8D29535B2941439
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobExecutionInformation
Id                          : Job01
JobManagerTask              : 
JobPreparationTask          : 
JobReleaseTask              : 
LastModified                : 7/25/2015 9:12:07 PM
Metadata                    : 
PoolInformation             : Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
PreviousState               : 
PreviousStateTransitionTime : 
Priority                    : 0
State                       : Active
StateTransitionTime         : 7/25/2015 9:12:07 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job01
```

<span data-ttu-id="fb3a2-115">Эта команда получает задание с ИДЕНТИФИКАТОРом Job01.</span><span class="sxs-lookup"><span data-stu-id="fb3a2-115">This command gets the job that has the ID Job01.</span></span>
<span data-ttu-id="fb3a2-116">Используйте командлет Get-AzureRmBatchAccountKeys для присвоения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="fb3a2-116">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="fb3a2-117">Пример 2: получение всех активных заданий для расписания заданий</span><span class="sxs-lookup"><span data-stu-id="fb3a2-117">Example 2: Get all active jobs for a job schedule</span></span>
```
PS C:\>Get-AzureBatchJob -JobScheduleId "JobSchedule27" -Filter "state eq 'active'" -BatchContext $Context
CommonEnvironmentSettings   : 
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
CreationTime                : 7/25/2015 9:15:44 PM
DisplayName                 : 
ETag                        : 0x8D2953633DD13E1
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobExecutionInformation
Id                          : JobSchedule27:job-1
JobManagerTask              : 
JobPreparationTask          : 
JobReleaseTask              : 
LastModified                : 7/25/2015 9:15:44 PM
Metadata                    : 
PoolInformation             : Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
PreviousState               : 
PreviousStateTransitionTime : 
Priority                    : 0
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:44 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/JobSchedule27:job-1
```

<span data-ttu-id="fb3a2-118">Эта команда получает активные задания для расписания задания с ИДЕНТИФИКАТОРом JobSchedule27.</span><span class="sxs-lookup"><span data-stu-id="fb3a2-118">This command gets the active jobs for the job schedule that has the ID JobSchedule27.</span></span>

### <span data-ttu-id="fb3a2-119">Пример 3: получение всех заданий в расписании заданий с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="fb3a2-119">Example 3: Gets all jobs under a job schedule by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchJobSchedule -Id "JobSchedule27" -BatchContext $Context | Get-AzureBatchJob -BatchContext $Context
CommonEnvironmentSettings   : 
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
CreationTime                : 7/25/2015 9:15:44 PM
DisplayName                 : 
ETag                        : 0x8D2953633DD13E1
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobExecutionInformation
Id                          : JobSchedule27:job-1
JobManagerTask              : 
JobPreparationTask          : 
JobReleaseTask              : 
LastModified                : 7/25/2015 9:15:44 PM
Metadata                    : 
PoolInformation             : Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
PreviousState               : 
PreviousStateTransitionTime : 
Priority                    : 0
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:44 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobs/JobSchedule27:job-1
```

<span data-ttu-id="fb3a2-120">Эта команда получает расписание заданий с ИД JobSchedule27 с помощью командлета Get-AzureBatchJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="fb3a2-120">This command gets the job schedule that has the ID JobSchedule27 by using the Get-AzureBatchJobSchedule cmdlet.</span></span>
<span data-ttu-id="fb3a2-121">Команда передает это расписание задания в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="fb3a2-121">The command passes that job schedule to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="fb3a2-122">Команда получает все задания для этого расписания задания.</span><span class="sxs-lookup"><span data-stu-id="fb3a2-122">The command gets all jobs for that job schedule.</span></span>

## <span data-ttu-id="fb3a2-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fb3a2-123">PARAMETERS</span></span>

### <span data-ttu-id="fb3a2-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="fb3a2-124">-BatchContext</span></span>
<span data-ttu-id="fb3a2-125">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="fb3a2-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="fb3a2-126">Чтобы получить объект **BatchAccountContext** , содержащий клавиши доступа для вашей подписки, используйте командлет Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="fb3a2-126">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="fb3a2-127">-Expand</span><span class="sxs-lookup"><span data-stu-id="fb3a2-127">-Expand</span></span>
<span data-ttu-id="fb3a2-128">Указывает предложение развертывания протокола Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="fb3a2-128">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="fb3a2-129">Укажите значение этого параметра, чтобы получить связанные сущности от основной сущности, которые вы получаете.</span><span class="sxs-lookup"><span data-stu-id="fb3a2-129">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="fb3a2-130">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="fb3a2-130">-Filter</span></span>
<span data-ttu-id="fb3a2-131">Задает предложение фильтра OData для заданий.</span><span class="sxs-lookup"><span data-stu-id="fb3a2-131">Specifies an OData filter clause for jobs.</span></span>
<span data-ttu-id="fb3a2-132">Если фильтр не указан, этот командлет возвращает все задания для учетной записи пакетной службы или расписания задания.</span><span class="sxs-lookup"><span data-stu-id="fb3a2-132">If you do not specify a filter, this cmdlet returns all jobs for the Batch account or job schedule.</span></span>

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

### <span data-ttu-id="fb3a2-133">-ID</span><span class="sxs-lookup"><span data-stu-id="fb3a2-133">-Id</span></span>
<span data-ttu-id="fb3a2-134">Указывает идентификатор задания, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="fb3a2-134">Specifies the ID of the job that this cmdlet gets.</span></span>
<span data-ttu-id="fb3a2-135">Подстановочные знаки указывать нельзя.</span><span class="sxs-lookup"><span data-stu-id="fb3a2-135">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb3a2-136">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="fb3a2-136">-JobSchedule</span></span>
<span data-ttu-id="fb3a2-137">Указывает объект **PSCloudJobSchedule** , который представляет расписание задания, содержащее задания.</span><span class="sxs-lookup"><span data-stu-id="fb3a2-137">Specifies a **PSCloudJobSchedule** object that represents the job schedule which contains the jobs.</span></span>
<span data-ttu-id="fb3a2-138">Чтобы получить объект **PSCloudJobSchedule** , используйте командлет Get-AzureBatchJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="fb3a2-138">To obtain a **PSCloudJobSchedule** object, use the Get-AzureBatchJobSchedule cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule
Parameter Sets: ParentObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb3a2-139">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="fb3a2-139">-JobScheduleId</span></span>
<span data-ttu-id="fb3a2-140">Указывает идентификатор расписания задания, содержащего задания.</span><span class="sxs-lookup"><span data-stu-id="fb3a2-140">Specifies the ID of the job schedule which contains the jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb3a2-141">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="fb3a2-141">-MaxCount</span></span>
<span data-ttu-id="fb3a2-142">Задает максимальное количество возвращаемых заданий.</span><span class="sxs-lookup"><span data-stu-id="fb3a2-142">Specifies the maximum number of jobs to return.</span></span>
<span data-ttu-id="fb3a2-143">Если вы задаете нулевое значение (0) или меньше, в командлете не используется верхний предел.</span><span class="sxs-lookup"><span data-stu-id="fb3a2-143">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="fb3a2-144">Значение по умолчанию — 1000.</span><span class="sxs-lookup"><span data-stu-id="fb3a2-144">The default value is 1000.</span></span>

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

### <span data-ttu-id="fb3a2-145">-SELECT</span><span class="sxs-lookup"><span data-stu-id="fb3a2-145">-Select</span></span>
<span data-ttu-id="fb3a2-146">Задает предложение SELECT OData.</span><span class="sxs-lookup"><span data-stu-id="fb3a2-146">Specifies an OData select clause.</span></span>
<span data-ttu-id="fb3a2-147">Укажите значение этого параметра, чтобы получить конкретные свойства, а не все свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="fb3a2-147">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="fb3a2-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb3a2-148">-DefaultProfile</span></span>
<span data-ttu-id="fb3a2-149">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fb3a2-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb3a2-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb3a2-150">CommonParameters</span></span>
<span data-ttu-id="fb3a2-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fb3a2-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb3a2-152">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb3a2-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb3a2-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fb3a2-153">INPUTS</span></span>

### <span data-ttu-id="fb3a2-154">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="fb3a2-154">BatchAccountContext</span></span>
<span data-ttu-id="fb3a2-155">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="fb3a2-155">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="fb3a2-156">PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="fb3a2-156">PSCloudJobSchedule</span></span>
<span data-ttu-id="fb3a2-157">Параметр "JobSchedule" принимает значение типа "PSCloudJobSchedule" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="fb3a2-157">Parameter 'JobSchedule' accepts value of type 'PSCloudJobSchedule' from the pipeline</span></span>

## <span data-ttu-id="fb3a2-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb3a2-158">OUTPUTS</span></span>

### <span data-ttu-id="fb3a2-159">PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="fb3a2-159">PSCloudJob</span></span>

## <span data-ttu-id="fb3a2-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="fb3a2-160">NOTES</span></span>

## <span data-ttu-id="fb3a2-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fb3a2-161">RELATED LINKS</span></span>

[<span data-ttu-id="fb3a2-162">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="fb3a2-162">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="fb3a2-163">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="fb3a2-163">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="fb3a2-164">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="fb3a2-164">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="fb3a2-165">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="fb3a2-165">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="fb3a2-166">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="fb3a2-166">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="fb3a2-167">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="fb3a2-167">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="fb3a2-168">Остановить-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="fb3a2-168">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="fb3a2-169">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="fb3a2-169">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


