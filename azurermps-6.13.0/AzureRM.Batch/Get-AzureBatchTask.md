---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 4B5FE41A-090B-4859-B021-05CF0A8B7882
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchTask.md
ms.openlocfilehash: 0229a44512aecc52b16650740d74ff177f83b9fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567819"
---
# <span data-ttu-id="0c70b-101">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="0c70b-101">Get-AzureBatchTask</span></span>

## <span data-ttu-id="0c70b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0c70b-102">SYNOPSIS</span></span>
<span data-ttu-id="0c70b-103">Возвращает пакетные задачи для задания.</span><span class="sxs-lookup"><span data-stu-id="0c70b-103">Gets the Batch tasks for a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c70b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0c70b-104">SYNTAX</span></span>

### <span data-ttu-id="0c70b-105">ODataFilter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0c70b-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchTask [-JobId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0c70b-106">Номер</span><span class="sxs-lookup"><span data-stu-id="0c70b-106">Id</span></span>
```
Get-AzureBatchTask [-JobId] <String> [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c70b-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="0c70b-107">ParentObject</span></span>
```
Get-AzureBatchTask [[-Job] <PSCloudJob>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0c70b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c70b-108">DESCRIPTION</span></span>
<span data-ttu-id="0c70b-109">Командлет **Get-AzureBatchTask** получает пакетные задачи Azure для пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="0c70b-109">The **Get-AzureBatchTask** cmdlet gets Azure Batch tasks for a Batch job.</span></span>
<span data-ttu-id="0c70b-110">Укажите задание с помощью параметра *JOBID* или параметра *задания* .</span><span class="sxs-lookup"><span data-stu-id="0c70b-110">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="0c70b-111">Чтобы получить одну задачу, укажите параметр *ID* .</span><span class="sxs-lookup"><span data-stu-id="0c70b-111">To get a single task, specify the *Id* parameter.</span></span>
<span data-ttu-id="0c70b-112">Вы можете указать параметр *Filter* , чтобы получить задачи, соответствующие фильтру Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="0c70b-112">You can specify the *Filter* parameter to get the tasks that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="0c70b-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0c70b-113">EXAMPLES</span></span>

### <span data-ttu-id="0c70b-114">Пример 1: получение задачи по ИДЕНТИФИКАТОРу</span><span class="sxs-lookup"><span data-stu-id="0c70b-114">Example 1: Get a task by ID</span></span>
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

<span data-ttu-id="0c70b-115">Эта команда получает задачу с ИДЕНТИФИКАТОРом Task03 в разделе задания Job01.</span><span class="sxs-lookup"><span data-stu-id="0c70b-115">This command gets the task with ID Task03 under job Job01.</span></span>
<span data-ttu-id="0c70b-116">Используйте командлет Get-AzureRmBatchAccountKeys для присвоения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="0c70b-116">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="0c70b-117">Пример 2: получение всех завершенных задач из указанного задания</span><span class="sxs-lookup"><span data-stu-id="0c70b-117">Example 2: Get all completed tasks from a specified job</span></span>
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

<span data-ttu-id="0c70b-118">Эта команда получает завершенные задачи из задания с ИДЕНТИФИКАТОРом Job02.</span><span class="sxs-lookup"><span data-stu-id="0c70b-118">This command gets the completed tasks from the job that has the ID Job02.</span></span>

## <span data-ttu-id="0c70b-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0c70b-119">PARAMETERS</span></span>

### <span data-ttu-id="0c70b-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="0c70b-120">-BatchContext</span></span>
<span data-ttu-id="0c70b-121">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="0c70b-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="0c70b-122">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="0c70b-122">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="0c70b-123">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="0c70b-123">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="0c70b-124">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="0c70b-124">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="0c70b-125">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="0c70b-125">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="0c70b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c70b-126">-DefaultProfile</span></span>
<span data-ttu-id="0c70b-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0c70b-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c70b-128">-Expand</span><span class="sxs-lookup"><span data-stu-id="0c70b-128">-Expand</span></span>
<span data-ttu-id="0c70b-129">Задает предложение развертывания OData.</span><span class="sxs-lookup"><span data-stu-id="0c70b-129">Specifies an OData expand clause.</span></span>
<span data-ttu-id="0c70b-130">Укажите значение этого параметра, чтобы получить связанные сущности основной сущности.</span><span class="sxs-lookup"><span data-stu-id="0c70b-130">Specify a value for this parameter to get associated entities of the main entity to get.</span></span>

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

### <span data-ttu-id="0c70b-131">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="0c70b-131">-Filter</span></span>
<span data-ttu-id="0c70b-132">Задает предложение фильтра OData для задач.</span><span class="sxs-lookup"><span data-stu-id="0c70b-132">Specifies an OData filter clause for tasks.</span></span>
<span data-ttu-id="0c70b-133">Если фильтр не указан, этот командлет возвращает все задачи для учетной записи или задания пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="0c70b-133">If you do not specify a filter, this cmdlet returns all tasks for the Batch account or job.</span></span>

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

### <span data-ttu-id="0c70b-134">-ID</span><span class="sxs-lookup"><span data-stu-id="0c70b-134">-Id</span></span>
<span data-ttu-id="0c70b-135">Указывает идентификатор задачи, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="0c70b-135">Specifies the ID of the task that this cmdlet gets.</span></span>
<span data-ttu-id="0c70b-136">Подстановочные знаки указывать нельзя.</span><span class="sxs-lookup"><span data-stu-id="0c70b-136">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="0c70b-137">-Job</span><span class="sxs-lookup"><span data-stu-id="0c70b-137">-Job</span></span>
<span data-ttu-id="0c70b-138">Указывает задание, содержащее задачи, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="0c70b-138">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="0c70b-139">Чтобы получить объект **PSCloudJob** , используйте командлет Get-AzureBatchJob.</span><span class="sxs-lookup"><span data-stu-id="0c70b-139">To obtain a **PSCloudJob** object, use the Get-AzureBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="0c70b-140">-JobId</span><span class="sxs-lookup"><span data-stu-id="0c70b-140">-JobId</span></span>
<span data-ttu-id="0c70b-141">Указывает идентификатор задания, содержащего задачи, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="0c70b-141">Specifies the ID of the job that contains the tasks that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0c70b-142">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="0c70b-142">-MaxCount</span></span>
<span data-ttu-id="0c70b-143">Задает максимальное количество возвращаемых задач.</span><span class="sxs-lookup"><span data-stu-id="0c70b-143">Specifies the maximum number of tasks to return.</span></span>
<span data-ttu-id="0c70b-144">Если вы задаете нулевое значение (0) или меньше, в командлете не используется верхний предел.</span><span class="sxs-lookup"><span data-stu-id="0c70b-144">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="0c70b-145">Значение по умолчанию — 1000.</span><span class="sxs-lookup"><span data-stu-id="0c70b-145">The default value is 1000.</span></span>

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

### <span data-ttu-id="0c70b-146">-SELECT</span><span class="sxs-lookup"><span data-stu-id="0c70b-146">-Select</span></span>
<span data-ttu-id="0c70b-147">Задает предложение SELECT OData.</span><span class="sxs-lookup"><span data-stu-id="0c70b-147">Specifies an OData select clause.</span></span>
<span data-ttu-id="0c70b-148">Укажите значение этого параметра, чтобы получить конкретные свойства, а не все свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="0c70b-148">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="0c70b-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c70b-149">CommonParameters</span></span>
<span data-ttu-id="0c70b-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0c70b-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c70b-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c70b-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c70b-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0c70b-152">INPUTS</span></span>

### <span data-ttu-id="0c70b-153">System. String</span><span class="sxs-lookup"><span data-stu-id="0c70b-153">System.String</span></span>

### <span data-ttu-id="0c70b-154">Microsoft.Azure.Commands.BatCH. Models. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="0c70b-154">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>
<span data-ttu-id="0c70b-155">Параметры: Job (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0c70b-155">Parameters: Job (ByValue)</span></span>

### <span data-ttu-id="0c70b-156">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0c70b-156">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="0c70b-157">Параметры: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0c70b-157">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="0c70b-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c70b-158">OUTPUTS</span></span>

### <span data-ttu-id="0c70b-159">Microsoft.Azure.Commands.BatCH. Models. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="0c70b-159">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

## <span data-ttu-id="0c70b-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="0c70b-160">NOTES</span></span>

## <span data-ttu-id="0c70b-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0c70b-161">RELATED LINKS</span></span>

[<span data-ttu-id="0c70b-162">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="0c70b-162">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="0c70b-163">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="0c70b-163">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="0c70b-164">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="0c70b-164">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="0c70b-165">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="0c70b-165">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="0c70b-166">Остановить-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="0c70b-166">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="0c70b-167">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="0c70b-167">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


