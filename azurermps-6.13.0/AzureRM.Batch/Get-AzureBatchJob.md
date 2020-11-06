---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 8BF49C4D-E7CD-4FD0-AFAC-9856239D24EC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJob.md
ms.openlocfilehash: 1a5f971e52da27eb2abeca02c4362eee9b9755c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565920"
---
# <span data-ttu-id="8dda7-101">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="8dda7-101">Get-AzureBatchJob</span></span>

## <span data-ttu-id="8dda7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8dda7-102">SYNOPSIS</span></span>
<span data-ttu-id="8dda7-103">Возвращает пакетные задания для учетной записи пакетной службы или расписания задания.</span><span class="sxs-lookup"><span data-stu-id="8dda7-103">Gets Batch jobs for a Batch account or job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8dda7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8dda7-104">SYNTAX</span></span>

### <span data-ttu-id="8dda7-105">ODataFilter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8dda7-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchJob [-JobScheduleId <String>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8dda7-106">Номер</span><span class="sxs-lookup"><span data-stu-id="8dda7-106">Id</span></span>
```
Get-AzureBatchJob [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8dda7-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="8dda7-107">ParentObject</span></span>
```
Get-AzureBatchJob [[-JobSchedule] <PSCloudJobSchedule>] [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8dda7-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8dda7-108">DESCRIPTION</span></span>
<span data-ttu-id="8dda7-109">Командлет **Get-AzureBatchJob** получает пакетные задания Azure для учетной записи пакетной службы, указанной в параметре *BatchAccountContext* .</span><span class="sxs-lookup"><span data-stu-id="8dda7-109">The **Get-AzureBatchJob** cmdlet gets the Azure Batch jobs for the Batch account specified by the *BatchAccountContext* parameter.</span></span>
<span data-ttu-id="8dda7-110">Вы можете использовать параметр *ID* для получения одного задания.</span><span class="sxs-lookup"><span data-stu-id="8dda7-110">You can use the *Id* parameter to get a single job.</span></span>
<span data-ttu-id="8dda7-111">С помощью параметра *Filter* можно получить задания, соответствующие фильтру Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="8dda7-111">You can use the *Filter* parameter to get the jobs that match an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="8dda7-112">Если вы задаете идентификатор расписания задания или экземпляр **PSCloudJobSchedule** , этот командлет возвращает только задания для этого расписания задания.</span><span class="sxs-lookup"><span data-stu-id="8dda7-112">If you supply a job schedule ID or **PSCloudJobSchedule** instance, this cmdlet returns only the jobs for that job schedule.</span></span>

## <span data-ttu-id="8dda7-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8dda7-113">EXAMPLES</span></span>

### <span data-ttu-id="8dda7-114">Пример 1: получение пакетного задания по ИДЕНТИФИКАТОРу</span><span class="sxs-lookup"><span data-stu-id="8dda7-114">Example 1: Get a Batch job by ID</span></span>
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

<span data-ttu-id="8dda7-115">Эта команда получает задание с ИДЕНТИФИКАТОРом Job01.</span><span class="sxs-lookup"><span data-stu-id="8dda7-115">This command gets the job that has the ID Job01.</span></span>
<span data-ttu-id="8dda7-116">Используйте командлет Get-AzureRmBatchAccountKeys для присвоения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="8dda7-116">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="8dda7-117">Пример 2: получение всех активных заданий для расписания заданий</span><span class="sxs-lookup"><span data-stu-id="8dda7-117">Example 2: Get all active jobs for a job schedule</span></span>
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

<span data-ttu-id="8dda7-118">Эта команда получает активные задания для расписания задания с ИДЕНТИФИКАТОРом JobSchedule27.</span><span class="sxs-lookup"><span data-stu-id="8dda7-118">This command gets the active jobs for the job schedule that has the ID JobSchedule27.</span></span>

### <span data-ttu-id="8dda7-119">Пример 3: получение всех заданий в расписании заданий с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="8dda7-119">Example 3: Gets all jobs under a job schedule by using the pipeline</span></span>
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

<span data-ttu-id="8dda7-120">Эта команда получает расписание заданий с ИД JobSchedule27 с помощью командлета Get-AzureBatchJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="8dda7-120">This command gets the job schedule that has the ID JobSchedule27 by using the Get-AzureBatchJobSchedule cmdlet.</span></span>
<span data-ttu-id="8dda7-121">Команда передает это расписание задания в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="8dda7-121">The command passes that job schedule to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8dda7-122">Команда получает все задания для этого расписания задания.</span><span class="sxs-lookup"><span data-stu-id="8dda7-122">The command gets all jobs for that job schedule.</span></span>

## <span data-ttu-id="8dda7-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8dda7-123">PARAMETERS</span></span>

### <span data-ttu-id="8dda7-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="8dda7-124">-BatchContext</span></span>
<span data-ttu-id="8dda7-125">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="8dda7-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8dda7-126">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="8dda7-126">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="8dda7-127">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="8dda7-127">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="8dda7-128">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="8dda7-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="8dda7-129">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="8dda7-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="8dda7-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dda7-130">-DefaultProfile</span></span>
<span data-ttu-id="8dda7-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8dda7-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8dda7-132">-Expand</span><span class="sxs-lookup"><span data-stu-id="8dda7-132">-Expand</span></span>
<span data-ttu-id="8dda7-133">Указывает предложение развертывания протокола Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="8dda7-133">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="8dda7-134">Укажите значение этого параметра, чтобы получить связанные сущности от основной сущности, которые вы получаете.</span><span class="sxs-lookup"><span data-stu-id="8dda7-134">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="8dda7-135">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="8dda7-135">-Filter</span></span>
<span data-ttu-id="8dda7-136">Задает предложение фильтра OData для заданий.</span><span class="sxs-lookup"><span data-stu-id="8dda7-136">Specifies an OData filter clause for jobs.</span></span>
<span data-ttu-id="8dda7-137">Если фильтр не указан, этот командлет возвращает все задания для учетной записи пакетной службы или расписания задания.</span><span class="sxs-lookup"><span data-stu-id="8dda7-137">If you do not specify a filter, this cmdlet returns all jobs for the Batch account or job schedule.</span></span>

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

### <span data-ttu-id="8dda7-138">-ID</span><span class="sxs-lookup"><span data-stu-id="8dda7-138">-Id</span></span>
<span data-ttu-id="8dda7-139">Указывает идентификатор задания, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="8dda7-139">Specifies the ID of the job that this cmdlet gets.</span></span>
<span data-ttu-id="8dda7-140">Подстановочные знаки указывать нельзя.</span><span class="sxs-lookup"><span data-stu-id="8dda7-140">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="8dda7-141">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="8dda7-141">-JobSchedule</span></span>
<span data-ttu-id="8dda7-142">Указывает объект **PSCloudJobSchedule** , который представляет расписание задания, содержащее задания.</span><span class="sxs-lookup"><span data-stu-id="8dda7-142">Specifies a **PSCloudJobSchedule** object that represents the job schedule which contains the jobs.</span></span>
<span data-ttu-id="8dda7-143">Чтобы получить объект **PSCloudJobSchedule** , используйте командлет Get-AzureBatchJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="8dda7-143">To obtain a **PSCloudJobSchedule** object, use the Get-AzureBatchJobSchedule cmdlet.</span></span>

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

### <span data-ttu-id="8dda7-144">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="8dda7-144">-JobScheduleId</span></span>
<span data-ttu-id="8dda7-145">Указывает идентификатор расписания задания, содержащего задания.</span><span class="sxs-lookup"><span data-stu-id="8dda7-145">Specifies the ID of the job schedule which contains the jobs.</span></span>

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

### <span data-ttu-id="8dda7-146">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="8dda7-146">-MaxCount</span></span>
<span data-ttu-id="8dda7-147">Задает максимальное количество возвращаемых заданий.</span><span class="sxs-lookup"><span data-stu-id="8dda7-147">Specifies the maximum number of jobs to return.</span></span>
<span data-ttu-id="8dda7-148">Если вы задаете нулевое значение (0) или меньше, в командлете не используется верхний предел.</span><span class="sxs-lookup"><span data-stu-id="8dda7-148">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="8dda7-149">Значение по умолчанию — 1000.</span><span class="sxs-lookup"><span data-stu-id="8dda7-149">The default value is 1000.</span></span>

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

### <span data-ttu-id="8dda7-150">-SELECT</span><span class="sxs-lookup"><span data-stu-id="8dda7-150">-Select</span></span>
<span data-ttu-id="8dda7-151">Задает предложение SELECT OData.</span><span class="sxs-lookup"><span data-stu-id="8dda7-151">Specifies an OData select clause.</span></span>
<span data-ttu-id="8dda7-152">Укажите значение этого параметра, чтобы получить конкретные свойства, а не все свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="8dda7-152">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="8dda7-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dda7-153">CommonParameters</span></span>
<span data-ttu-id="8dda7-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8dda7-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dda7-155">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8dda7-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dda7-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8dda7-156">INPUTS</span></span>

### <span data-ttu-id="8dda7-157">System. String</span><span class="sxs-lookup"><span data-stu-id="8dda7-157">System.String</span></span>

### <span data-ttu-id="8dda7-158">Microsoft.Azure.Commands.BatCH. Models. PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8dda7-158">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>
<span data-ttu-id="8dda7-159">Параметры: JobSchedule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8dda7-159">Parameters: JobSchedule (ByValue)</span></span>

### <span data-ttu-id="8dda7-160">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8dda7-160">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="8dda7-161">Параметры: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8dda7-161">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="8dda7-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8dda7-162">OUTPUTS</span></span>

### <span data-ttu-id="8dda7-163">Microsoft.Azure.Commands.BatCH. Models. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="8dda7-163">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

## <span data-ttu-id="8dda7-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="8dda7-164">NOTES</span></span>

## <span data-ttu-id="8dda7-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8dda7-165">RELATED LINKS</span></span>

[<span data-ttu-id="8dda7-166">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="8dda7-166">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="8dda7-167">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="8dda7-167">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="8dda7-168">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="8dda7-168">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="8dda7-169">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8dda7-169">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="8dda7-170">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="8dda7-170">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="8dda7-171">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="8dda7-171">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="8dda7-172">Остановить-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="8dda7-172">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="8dda7-173">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="8dda7-173">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


