---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 2DF5FB4D-A5CB-439C-AC6F-DF2130AF33EC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchComputeNodeScheduling.md
ms.openlocfilehash: 778347394e9793b95434e1b308bbdb4e28fc0915
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568098"
---
# <span data-ttu-id="aed6c-101">Disable-AzureBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="aed6c-101">Disable-AzureBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="aed6c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aed6c-102">SYNOPSIS</span></span>
<span data-ttu-id="aed6c-103">Отключает планирование задач на заданном вычислительном узле.</span><span class="sxs-lookup"><span data-stu-id="aed6c-103">Disables task scheduling on the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aed6c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aed6c-104">SYNTAX</span></span>

### <span data-ttu-id="aed6c-105">ID (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="aed6c-105">Id (Default)</span></span>
```
Disable-AzureBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String>
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aed6c-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="aed6c-106">InputObject</span></span>
```
Disable-AzureBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>]
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aed6c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aed6c-107">DESCRIPTION</span></span>
<span data-ttu-id="aed6c-108">Командлет **Disable-AzureBatchComputeNodeScheduling** отключает планирование задач на заданном вычислительном узле.</span><span class="sxs-lookup"><span data-stu-id="aed6c-108">The **Disable-AzureBatchComputeNodeScheduling** cmdlet disables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="aed6c-109">Вычислительный узел — это виртуальная машина Azure, выделенная для определенной рабочей нагрузки приложения.</span><span class="sxs-lookup"><span data-stu-id="aed6c-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>
<span data-ttu-id="aed6c-110">При отключении планирования задач на вычислительном узле вы также сможете определить, что делать в очереди задач узла.</span><span class="sxs-lookup"><span data-stu-id="aed6c-110">When you disable task scheduling on a compute node you will also have the option of determining what to do about jobs currently in the node's task queue.</span></span>
<span data-ttu-id="aed6c-111">**Disable-AzureBatchComputeNodeScheduling** позволяет выполнять указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="aed6c-111">**Disable-AzureBatchComputeNodeScheduling** lets you do the following:</span></span> 

- <span data-ttu-id="aed6c-112">Прервать задачи и вернуть их в очередь заданий.</span><span class="sxs-lookup"><span data-stu-id="aed6c-112">Terminate the tasks and put them back in the job queue.</span></span>
<span data-ttu-id="aed6c-113">Это позволяет перепланировать эти задачи на другом вычислительном узле.</span><span class="sxs-lookup"><span data-stu-id="aed6c-113">This enables those tasks to be rescheduled on another compute node.</span></span> 
- <span data-ttu-id="aed6c-114">Завершите задачи и удалите их из очереди заданий.</span><span class="sxs-lookup"><span data-stu-id="aed6c-114">Terminate the tasks and remove them from the job queue.</span></span>
<span data-ttu-id="aed6c-115">Задачи, остановленные таким образом, не будут перепланированы.</span><span class="sxs-lookup"><span data-stu-id="aed6c-115">Tasks stopped in this manner will not be rescheduled.</span></span> 
- <span data-ttu-id="aed6c-116">Дождитесь завершения всех задач, выполняемых в настоящее время, а затем отключите планирование задач на узле COMPUTE Node.</span><span class="sxs-lookup"><span data-stu-id="aed6c-116">Wait for all the tasks currently being executed to complete and then disable task scheduling on the compute node.</span></span> 
- <span data-ttu-id="aed6c-117">Дождитесь завершения всех выполняемых задач и истечения срока хранения данных, а затем отключите планирование задач на узле COMPUTE Node.</span><span class="sxs-lookup"><span data-stu-id="aed6c-117">Wait for all the running tasks to complete and all the data retention periods to expire, and then disable task scheduling on the compute node.</span></span>

## <span data-ttu-id="aed6c-118">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aed6c-118">EXAMPLES</span></span>

### <span data-ttu-id="aed6c-119">Пример 1: отключение планирования задач на вычислительном узле</span><span class="sxs-lookup"><span data-stu-id="aed6c-119">Example 1: Disable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Disable-AzureBatchComputeNodeScheduling -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="aed6c-120">Эти команды отключают расписание задач на COMPUTE node TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="aed6c-120">These commands disable task schedule on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="aed6c-121">Для этого первой командой в примере создается ссылка на объект для contosobatchaccount учетной записи пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="aed6c-121">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="aed6c-122">Эта ссылка на объект хранится в переменной с именем $context.</span><span class="sxs-lookup"><span data-stu-id="aed6c-122">This object reference is stored in a variable named $context.</span></span>

<span data-ttu-id="aed6c-123">Вторая команда использует эту ссылку на объект и командлет **Disable-AzureBatchComputeNodeScheduling** для подключения к пулу myPool и отключения планирования задач на узле TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="aed6c-123">The second command then uses this object reference and the **Disable-AzureBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and disable task scheduling on node tvm-1783593343_34-20151117t222514z.</span></span>

<span data-ttu-id="aed6c-124">Так как параметр *DisableComputeNodeSchedulingOptions* не включал в себя все задачи, которые выполняются на вычислительном узле, они будут повторно помещены в очередь.</span><span class="sxs-lookup"><span data-stu-id="aed6c-124">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute node will be requeued.</span></span>

### <span data-ttu-id="aed6c-125">Пример 2: отключение планирования задач на всех вычислительных узлах в пуле</span><span class="sxs-lookup"><span data-stu-id="aed6c-125">Example 2: Disable task scheduling on all compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzureBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Disable-AzureBatchComputeNodeScheduling -BatchContext $Context
```

<span data-ttu-id="aed6c-126">Эти команды отключают планирование задач на всех узлах компьютера в Pool06 пула пакетов.</span><span class="sxs-lookup"><span data-stu-id="aed6c-126">These commands disable task scheduling on all the computer nodes in the batch pool Pool06.</span></span>
<span data-ttu-id="aed6c-127">Для выполнения этой задачи в первой команде в примере создается ссылка на объект для учетной записи пакетной contosobatchaccount с помощью ключа учетной записи.</span><span class="sxs-lookup"><span data-stu-id="aed6c-127">To perform this task, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="aed6c-128">Эта ссылка на объект хранится в переменной с именем $context.</span><span class="sxs-lookup"><span data-stu-id="aed6c-128">This object reference is stored in a variable named $context.</span></span>

<span data-ttu-id="aed6c-129">Во второй команде в примере используется ссылка на объект и **Get-AzureBatchComputeNode** , чтобы вернуть коллекцию всех вычислительных узлов, обнаруженных в Pool06.</span><span class="sxs-lookup"><span data-stu-id="aed6c-129">The second command in the example then uses this object reference and **Get-AzureBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="aed6c-130">После этого коллекция передается на командлет **Disable-AzureBatchComputeNodeScheduling** , чтобы отключить планирование задач на каждом из вычислительных узлов коллекции.</span><span class="sxs-lookup"><span data-stu-id="aed6c-130">That collection is then piped to then **Disable-AzureBatchComputeNodeScheduling** cmdlet to disable task scheduling on each compute node in the collection.</span></span>

<span data-ttu-id="aed6c-131">Так как параметр *DisableComputeNodeSchedulingOptions* не включал в себя все задачи, которые выполняются на вычислительных узлах, они будут повторно помещены в очередь.</span><span class="sxs-lookup"><span data-stu-id="aed6c-131">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute nodes will be requeued.</span></span>

## <span data-ttu-id="aed6c-132">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aed6c-132">PARAMETERS</span></span>

### <span data-ttu-id="aed6c-133">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="aed6c-133">-BatchContext</span></span>
<span data-ttu-id="aed6c-134">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="aed6c-134">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="aed6c-135">Чтобы получить объект **BatchAccountContext** , содержащий клавиши доступа для вашей подписки, используйте командлет Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="aed6c-135">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="aed6c-136">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="aed6c-136">-ComputeNode</span></span>
<span data-ttu-id="aed6c-137">Указывает ссылку на объект на вычислительный узел, если планирование задач отключено.</span><span class="sxs-lookup"><span data-stu-id="aed6c-137">Specifies an object reference to the compute node where task scheduling is disabled.</span></span>
<span data-ttu-id="aed6c-138">Эта ссылка на объект создается с помощью командлета Get-AzureBatchComputeNode и сохраняет возвращаемый объект COMPUTE Node в переменной.</span><span class="sxs-lookup"><span data-stu-id="aed6c-138">This object reference is created by using the Get-AzureBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aed6c-139">-DisableSchedulingOption</span><span class="sxs-lookup"><span data-stu-id="aed6c-139">-DisableSchedulingOption</span></span>
<span data-ttu-id="aed6c-140">Указывает, как этот командлет обрабатывает все задачи, которые выполняются в данный момент на узле компьютера, где планирование отключено.</span><span class="sxs-lookup"><span data-stu-id="aed6c-140">Specifies how this cmdlet deals with any tasks currently running on the computer node where scheduling is being disabled.</span></span>
<span data-ttu-id="aed6c-141">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="aed6c-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="aed6c-142">Поочередно.</span><span class="sxs-lookup"><span data-stu-id="aed6c-142">Requeue.</span></span>
<span data-ttu-id="aed6c-143">Задачи немедленно останавливаются и возвращаются в очередь заданий.</span><span class="sxs-lookup"><span data-stu-id="aed6c-143">Tasks are stopped immediately and returned to the job queue.</span></span>
<span data-ttu-id="aed6c-144">Это позволяет перепланировать задачи на другом вычислительном узле.</span><span class="sxs-lookup"><span data-stu-id="aed6c-144">This enables the tasks to be rescheduled on another compute node.</span></span>
<span data-ttu-id="aed6c-145">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="aed6c-145">This is the default value.</span></span> 
- <span data-ttu-id="aed6c-146">Разорван.</span><span class="sxs-lookup"><span data-stu-id="aed6c-146">Terminate.</span></span>
<span data-ttu-id="aed6c-147">Задачи немедленно останавливаются и удаляются из очереди заданий.</span><span class="sxs-lookup"><span data-stu-id="aed6c-147">Tasks are stopped immediately and removed from the job queue.</span></span>
<span data-ttu-id="aed6c-148">Эти задачи не будут перепланированы.</span><span class="sxs-lookup"><span data-stu-id="aed6c-148">These tasks will not be rescheduled.</span></span> 
- <span data-ttu-id="aed6c-149">TaskCompletion.</span><span class="sxs-lookup"><span data-stu-id="aed6c-149">TaskCompletion.</span></span>
<span data-ttu-id="aed6c-150">Запущенные в данный момент задачи можно выполнить, прежде чем планирование задач будет отключено на вычислительном узле.</span><span class="sxs-lookup"><span data-stu-id="aed6c-150">Currently running tasks will be able to complete before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="aed6c-151">На этом узле не будут планироваться новые задачи.</span><span class="sxs-lookup"><span data-stu-id="aed6c-151">No new tasks will be scheduled on this node.</span></span> 
- <span data-ttu-id="aed6c-152">RetainedData.</span><span class="sxs-lookup"><span data-stu-id="aed6c-152">RetainedData.</span></span>
<span data-ttu-id="aed6c-153">Запущенные в настоящее время задачи смогут завершить работу, и срок хранения данных будет ограничен, прежде чем планирование задач на узле COMPUTE node станет недоступным.</span><span class="sxs-lookup"><span data-stu-id="aed6c-153">Currently running tasks will be able to complete and data retention periods will be able to expire before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="aed6c-154">На этом узле не будут планироваться новые задачи.</span><span class="sxs-lookup"><span data-stu-id="aed6c-154">No new tasks will be scheduled on this node.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.DisableComputeNodeSchedulingOption]
Parameter Sets: (All)
Aliases: 
Accepted values: Requeue, Terminate, TaskCompletion

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aed6c-155">-ID</span><span class="sxs-lookup"><span data-stu-id="aed6c-155">-Id</span></span>
<span data-ttu-id="aed6c-156">Указывает идентификатор вычислительного узла, на котором отключено планирование задач.</span><span class="sxs-lookup"><span data-stu-id="aed6c-156">Specifies the ID of the compute node where task scheduling is disabled.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aed6c-157">-PoolId</span><span class="sxs-lookup"><span data-stu-id="aed6c-157">-PoolId</span></span>
<span data-ttu-id="aed6c-158">Указывает идентификатор пула пакетов, содержащего вычислительный узел, для которого планирование задач отключено.</span><span class="sxs-lookup"><span data-stu-id="aed6c-158">Specifies the ID of the batch pool that contains the compute node where task scheduling is disabled.</span></span>

<span data-ttu-id="aed6c-159">Если вы используете параметр *PoolId* , не используйте параметр *ComputeNode* в той же команде.</span><span class="sxs-lookup"><span data-stu-id="aed6c-159">If you use the *PoolId* parameter, do not use the *ComputeNode* parameter in that same command.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aed6c-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aed6c-160">-DefaultProfile</span></span>
<span data-ttu-id="aed6c-161">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aed6c-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aed6c-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aed6c-162">CommonParameters</span></span>
<span data-ttu-id="aed6c-163">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aed6c-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aed6c-164">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aed6c-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aed6c-165">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aed6c-165">INPUTS</span></span>

### <span data-ttu-id="aed6c-166">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="aed6c-166">BatchAccountContext</span></span>
<span data-ttu-id="aed6c-167">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="aed6c-167">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="aed6c-168">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="aed6c-168">PSComputeNode</span></span>
<span data-ttu-id="aed6c-169">Параметр "ComputeNode" принимает значение типа "PSComputeNode" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="aed6c-169">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="aed6c-170">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aed6c-170">OUTPUTS</span></span>

## <span data-ttu-id="aed6c-171">Пуск</span><span class="sxs-lookup"><span data-stu-id="aed6c-171">NOTES</span></span>

## <span data-ttu-id="aed6c-172">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aed6c-172">RELATED LINKS</span></span>

[<span data-ttu-id="aed6c-173">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="aed6c-173">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="aed6c-174">Enable-AzureBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="aed6c-174">Enable-AzureBatchComputeNodeScheduling</span></span>](./Enable-AzureBatchComputeNodeScheduling.md)


