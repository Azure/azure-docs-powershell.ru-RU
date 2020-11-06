---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 2DF5FB4D-A5CB-439C-AC6F-DF2130AF33EC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/disable-azurebatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchComputeNodeScheduling.md
ms.openlocfilehash: 40eb6d3cfd3961c876a5da07ced1ebcf383166e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570263"
---
# <span data-ttu-id="3e321-101">Disable-AzureBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="3e321-101">Disable-AzureBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="3e321-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3e321-102">SYNOPSIS</span></span>
<span data-ttu-id="3e321-103">Отключает планирование задач на заданном вычислительном узле.</span><span class="sxs-lookup"><span data-stu-id="3e321-103">Disables task scheduling on the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e321-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3e321-104">SYNTAX</span></span>

### <span data-ttu-id="3e321-105">ID (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3e321-105">Id (Default)</span></span>
```
Disable-AzureBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String>
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e321-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="3e321-106">InputObject</span></span>
```
Disable-AzureBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>]
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e321-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e321-107">DESCRIPTION</span></span>
<span data-ttu-id="3e321-108">Командлет **Disable-AzureBatchComputeNodeScheduling** отключает планирование задач на заданном вычислительном узле.</span><span class="sxs-lookup"><span data-stu-id="3e321-108">The **Disable-AzureBatchComputeNodeScheduling** cmdlet disables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="3e321-109">Вычислительный узел — это виртуальная машина Azure, выделенная для определенной рабочей нагрузки приложения.</span><span class="sxs-lookup"><span data-stu-id="3e321-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>
<span data-ttu-id="3e321-110">При отключении планирования задач на вычислительном узле вы также сможете определить, что делать в очереди задач узла.</span><span class="sxs-lookup"><span data-stu-id="3e321-110">When you disable task scheduling on a compute node you will also have the option of determining what to do about jobs currently in the node's task queue.</span></span>
<span data-ttu-id="3e321-111">**Disable-AzureBatchComputeNodeScheduling** позволяет выполнять указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="3e321-111">**Disable-AzureBatchComputeNodeScheduling** lets you do the following:</span></span> 

- <span data-ttu-id="3e321-112">Прервать задачи и вернуть их в очередь заданий.</span><span class="sxs-lookup"><span data-stu-id="3e321-112">Terminate the tasks and put them back in the job queue.</span></span>
<span data-ttu-id="3e321-113">Это позволяет перепланировать эти задачи на другом вычислительном узле.</span><span class="sxs-lookup"><span data-stu-id="3e321-113">This enables those tasks to be rescheduled on another compute node.</span></span> 
- <span data-ttu-id="3e321-114">Завершите задачи и удалите их из очереди заданий.</span><span class="sxs-lookup"><span data-stu-id="3e321-114">Terminate the tasks and remove them from the job queue.</span></span>
<span data-ttu-id="3e321-115">Задачи, остановленные таким образом, не будут перепланированы.</span><span class="sxs-lookup"><span data-stu-id="3e321-115">Tasks stopped in this manner will not be rescheduled.</span></span> 
- <span data-ttu-id="3e321-116">Дождитесь завершения всех задач, выполняемых в настоящее время, а затем отключите планирование задач на узле COMPUTE Node.</span><span class="sxs-lookup"><span data-stu-id="3e321-116">Wait for all the tasks currently being executed to complete and then disable task scheduling on the compute node.</span></span> 
- <span data-ttu-id="3e321-117">Дождитесь завершения всех выполняемых задач и истечения срока хранения данных, а затем отключите планирование задач на узле COMPUTE Node.</span><span class="sxs-lookup"><span data-stu-id="3e321-117">Wait for all the running tasks to complete and all the data retention periods to expire, and then disable task scheduling on the compute node.</span></span>

## <span data-ttu-id="3e321-118">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3e321-118">EXAMPLES</span></span>

### <span data-ttu-id="3e321-119">Пример 1: отключение планирования задач на вычислительном узле</span><span class="sxs-lookup"><span data-stu-id="3e321-119">Example 1: Disable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Disable-AzureBatchComputeNodeScheduling -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="3e321-120">Эти команды отключают расписание задач на COMPUTE node TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="3e321-120">These commands disable task schedule on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="3e321-121">Для этого первой командой в примере создается ссылка на объект для contosobatchaccount учетной записи пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="3e321-121">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="3e321-122">Эта ссылка на объект хранится в переменной с именем $context.</span><span class="sxs-lookup"><span data-stu-id="3e321-122">This object reference is stored in a variable named $context.</span></span>

<span data-ttu-id="3e321-123">Вторая команда использует эту ссылку на объект и командлет **Disable-AzureBatchComputeNodeScheduling** для подключения к пулу myPool и отключения планирования задач на узле TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="3e321-123">The second command then uses this object reference and the **Disable-AzureBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and disable task scheduling on node tvm-1783593343_34-20151117t222514z.</span></span>

<span data-ttu-id="3e321-124">Так как параметр *DisableComputeNodeSchedulingOptions* не включал в себя все задачи, которые выполняются на вычислительном узле, они будут повторно помещены в очередь.</span><span class="sxs-lookup"><span data-stu-id="3e321-124">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute node will be requeued.</span></span>

### <span data-ttu-id="3e321-125">Пример 2: отключение планирования задач на всех вычислительных узлах в пуле</span><span class="sxs-lookup"><span data-stu-id="3e321-125">Example 2: Disable task scheduling on all compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzureBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Disable-AzureBatchComputeNodeScheduling -BatchContext $Context
```

<span data-ttu-id="3e321-126">Эти команды отключают планирование задач на всех узлах компьютера в Pool06 пула пакетов.</span><span class="sxs-lookup"><span data-stu-id="3e321-126">These commands disable task scheduling on all the computer nodes in the batch pool Pool06.</span></span>
<span data-ttu-id="3e321-127">Для выполнения этой задачи в первой команде в примере создается ссылка на объект для учетной записи пакетной contosobatchaccount с помощью ключа учетной записи.</span><span class="sxs-lookup"><span data-stu-id="3e321-127">To perform this task, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="3e321-128">Эта ссылка на объект хранится в переменной с именем $context.</span><span class="sxs-lookup"><span data-stu-id="3e321-128">This object reference is stored in a variable named $context.</span></span>

<span data-ttu-id="3e321-129">Во второй команде в примере используется ссылка на объект и **Get-AzureBatchComputeNode** , чтобы вернуть коллекцию всех вычислительных узлов, обнаруженных в Pool06.</span><span class="sxs-lookup"><span data-stu-id="3e321-129">The second command in the example then uses this object reference and **Get-AzureBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="3e321-130">После этого коллекция передается на командлет **Disable-AzureBatchComputeNodeScheduling** , чтобы отключить планирование задач на каждом из вычислительных узлов коллекции.</span><span class="sxs-lookup"><span data-stu-id="3e321-130">That collection is then piped to then **Disable-AzureBatchComputeNodeScheduling** cmdlet to disable task scheduling on each compute node in the collection.</span></span>

<span data-ttu-id="3e321-131">Так как параметр *DisableComputeNodeSchedulingOptions* не включал в себя все задачи, которые выполняются на вычислительных узлах, они будут повторно помещены в очередь.</span><span class="sxs-lookup"><span data-stu-id="3e321-131">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute nodes will be requeued.</span></span>

## <span data-ttu-id="3e321-132">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3e321-132">PARAMETERS</span></span>

### <span data-ttu-id="3e321-133">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="3e321-133">-BatchContext</span></span>
<span data-ttu-id="3e321-134">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="3e321-134">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="3e321-135">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="3e321-135">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="3e321-136">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="3e321-136">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="3e321-137">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="3e321-137">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="3e321-138">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="3e321-138">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e321-139">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="3e321-139">-ComputeNode</span></span>
<span data-ttu-id="3e321-140">Указывает ссылку на объект на вычислительный узел, если планирование задач отключено.</span><span class="sxs-lookup"><span data-stu-id="3e321-140">Specifies an object reference to the compute node where task scheduling is disabled.</span></span>
<span data-ttu-id="3e321-141">Эта ссылка на объект создается с помощью командлета Get-AzureBatchComputeNode и сохраняет возвращаемый объект COMPUTE Node в переменной.</span><span class="sxs-lookup"><span data-stu-id="3e321-141">This object reference is created by using the Get-AzureBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

```yaml
Type: PSComputeNode
Parameter Sets: InputObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e321-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e321-142">-DefaultProfile</span></span>
<span data-ttu-id="3e321-143">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3e321-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e321-144">-DisableSchedulingOption</span><span class="sxs-lookup"><span data-stu-id="3e321-144">-DisableSchedulingOption</span></span>
<span data-ttu-id="3e321-145">Указывает, как этот командлет обрабатывает все задачи, которые выполняются в данный момент на узле компьютера, где планирование отключено.</span><span class="sxs-lookup"><span data-stu-id="3e321-145">Specifies how this cmdlet deals with any tasks currently running on the computer node where scheduling is being disabled.</span></span>
<span data-ttu-id="3e321-146">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3e321-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3e321-147">Поочередно.</span><span class="sxs-lookup"><span data-stu-id="3e321-147">Requeue.</span></span>
<span data-ttu-id="3e321-148">Задачи немедленно останавливаются и возвращаются в очередь заданий.</span><span class="sxs-lookup"><span data-stu-id="3e321-148">Tasks are stopped immediately and returned to the job queue.</span></span>
<span data-ttu-id="3e321-149">Это позволяет перепланировать задачи на другом вычислительном узле.</span><span class="sxs-lookup"><span data-stu-id="3e321-149">This enables the tasks to be rescheduled on another compute node.</span></span>
<span data-ttu-id="3e321-150">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3e321-150">This is the default value.</span></span> 
- <span data-ttu-id="3e321-151">Разорван.</span><span class="sxs-lookup"><span data-stu-id="3e321-151">Terminate.</span></span>
<span data-ttu-id="3e321-152">Задачи немедленно останавливаются и удаляются из очереди заданий.</span><span class="sxs-lookup"><span data-stu-id="3e321-152">Tasks are stopped immediately and removed from the job queue.</span></span>
<span data-ttu-id="3e321-153">Эти задачи не будут перепланированы.</span><span class="sxs-lookup"><span data-stu-id="3e321-153">These tasks will not be rescheduled.</span></span> 
- <span data-ttu-id="3e321-154">TaskCompletion.</span><span class="sxs-lookup"><span data-stu-id="3e321-154">TaskCompletion.</span></span>
<span data-ttu-id="3e321-155">Запущенные в данный момент задачи можно выполнить, прежде чем планирование задач будет отключено на вычислительном узле.</span><span class="sxs-lookup"><span data-stu-id="3e321-155">Currently running tasks will be able to complete before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="3e321-156">На этом узле не будут планироваться новые задачи.</span><span class="sxs-lookup"><span data-stu-id="3e321-156">No new tasks will be scheduled on this node.</span></span> 
- <span data-ttu-id="3e321-157">RetainedData.</span><span class="sxs-lookup"><span data-stu-id="3e321-157">RetainedData.</span></span>
<span data-ttu-id="3e321-158">Запущенные в настоящее время задачи смогут завершить работу, и срок хранения данных будет ограничен, прежде чем планирование задач на узле COMPUTE node станет недоступным.</span><span class="sxs-lookup"><span data-stu-id="3e321-158">Currently running tasks will be able to complete and data retention periods will be able to expire before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="3e321-159">На этом узле не будут планироваться новые задачи.</span><span class="sxs-lookup"><span data-stu-id="3e321-159">No new tasks will be scheduled on this node.</span></span>

```yaml
Type: DisableComputeNodeSchedulingOption
Parameter Sets: (All)
Aliases: 
Accepted values: Requeue, Terminate, TaskCompletion

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e321-160">-ID</span><span class="sxs-lookup"><span data-stu-id="3e321-160">-Id</span></span>
<span data-ttu-id="3e321-161">Указывает идентификатор вычислительного узла, на котором отключено планирование задач.</span><span class="sxs-lookup"><span data-stu-id="3e321-161">Specifies the ID of the compute node where task scheduling is disabled.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e321-162">-PoolId</span><span class="sxs-lookup"><span data-stu-id="3e321-162">-PoolId</span></span>
<span data-ttu-id="3e321-163">Указывает идентификатор пула пакетов, содержащего вычислительный узел, для которого планирование задач отключено.</span><span class="sxs-lookup"><span data-stu-id="3e321-163">Specifies the ID of the batch pool that contains the compute node where task scheduling is disabled.</span></span>

<span data-ttu-id="3e321-164">Если вы используете параметр *PoolId* , не используйте параметр *ComputeNode* в той же команде.</span><span class="sxs-lookup"><span data-stu-id="3e321-164">If you use the *PoolId* parameter, do not use the *ComputeNode* parameter in that same command.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e321-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e321-165">CommonParameters</span></span>
<span data-ttu-id="3e321-166">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3e321-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e321-167">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e321-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e321-168">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3e321-168">INPUTS</span></span>

### <span data-ttu-id="3e321-169">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="3e321-169">BatchAccountContext</span></span>
<span data-ttu-id="3e321-170">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="3e321-170">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="3e321-171">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="3e321-171">PSComputeNode</span></span>
<span data-ttu-id="3e321-172">Параметр "ComputeNode" принимает значение типа "PSComputeNode" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="3e321-172">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="3e321-173">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e321-173">OUTPUTS</span></span>

## <span data-ttu-id="3e321-174">Пуск</span><span class="sxs-lookup"><span data-stu-id="3e321-174">NOTES</span></span>

## <span data-ttu-id="3e321-175">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3e321-175">RELATED LINKS</span></span>

[<span data-ttu-id="3e321-176">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="3e321-176">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="3e321-177">Enable-AzureBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="3e321-177">Enable-AzureBatchComputeNodeScheduling</span></span>](./Enable-AzureBatchComputeNodeScheduling.md)


