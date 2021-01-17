---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2DF5FB4D-A5CB-439C-AC6F-DF2130AF33EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 9e93d6fd17d4ba308e6d5752554fb03639fce769
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407063"
---
# <span data-ttu-id="4740a-101">Disable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="4740a-101">Disable-AzBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="4740a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4740a-102">SYNOPSIS</span></span>
<span data-ttu-id="4740a-103">Отключает планирование задач для указанного узла вычислений.</span><span class="sxs-lookup"><span data-stu-id="4740a-103">Disables task scheduling on the specified compute node.</span></span>

## <span data-ttu-id="4740a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4740a-104">SYNTAX</span></span>

### <span data-ttu-id="4740a-105">ИД (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4740a-105">Id (Default)</span></span>
```
Disable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String>
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4740a-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="4740a-106">InputObject</span></span>
```
Disable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>]
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4740a-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4740a-107">DESCRIPTION</span></span>
<span data-ttu-id="4740a-108">**Cmdlet Disable-AzBatchComputeNodeScheduling** отключает планирование задач в указанном узле вычислений.</span><span class="sxs-lookup"><span data-stu-id="4740a-108">The **Disable-AzBatchComputeNodeScheduling** cmdlet disables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="4740a-109">Узел вычислений — это виртуальная машинка Azure, выделенная для конкретной рабочей нагрузки приложения.</span><span class="sxs-lookup"><span data-stu-id="4740a-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>
<span data-ttu-id="4740a-110">Если отключить планирование задач на узле компьютеров, вы также сможете определить, что делать с заданиями, которые в настоящий момент находятся в очереди задач узла.</span><span class="sxs-lookup"><span data-stu-id="4740a-110">When you disable task scheduling on a compute node you will also have the option of determining what to do about jobs currently in the node's task queue.</span></span>
<span data-ttu-id="4740a-111">**Disable-AzBatchComputeNodeScheduling** позволяет:</span><span class="sxs-lookup"><span data-stu-id="4740a-111">**Disable-AzBatchComputeNodeScheduling** lets you do the following:</span></span> 
- <span data-ttu-id="4740a-112">Прервать задачи и поместить их обратно в очередь заданий.</span><span class="sxs-lookup"><span data-stu-id="4740a-112">Terminate the tasks and put them back in the job queue.</span></span>
<span data-ttu-id="4740a-113">Это позволяет перепланировать эти задачи на другом узле компьютеров.</span><span class="sxs-lookup"><span data-stu-id="4740a-113">This enables those tasks to be rescheduled on another compute node.</span></span> 
- <span data-ttu-id="4740a-114">Завершайте задачи и удаляйте их из очереди заданий.</span><span class="sxs-lookup"><span data-stu-id="4740a-114">Terminate the tasks and remove them from the job queue.</span></span>
<span data-ttu-id="4740a-115">Задачи, остановленные таким способом, не будут запланированы повторно.</span><span class="sxs-lookup"><span data-stu-id="4740a-115">Tasks stopped in this manner will not be rescheduled.</span></span> 
- <span data-ttu-id="4740a-116">Дождите завершения всех задач, которые выполняются в данный момент, а затем отключили планирование задач на узле вычислений.</span><span class="sxs-lookup"><span data-stu-id="4740a-116">Wait for all the tasks currently being executed to complete and then disable task scheduling on the compute node.</span></span> 
- <span data-ttu-id="4740a-117">Дождите завершения всех задач и истечения всех периодов хранения данных, а затем отключаете планирование задач на узле компьютеров.</span><span class="sxs-lookup"><span data-stu-id="4740a-117">Wait for all the running tasks to complete and all the data retention periods to expire, and then disable task scheduling on the compute node.</span></span>

## <span data-ttu-id="4740a-118">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4740a-118">EXAMPLES</span></span>

### <span data-ttu-id="4740a-119">Пример 1. Отключение планирования задач на узле вычислений</span><span class="sxs-lookup"><span data-stu-id="4740a-119">Example 1: Disable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Disable-AzBatchComputeNodeScheduling -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="4740a-120">Эти команды отключат расписание задач на узле вычислений tvm-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="4740a-120">These commands disable task schedule on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="4740a-121">Для этого первая команда в примере создает ссылку на ключи учетных записей для пакетной учетной записи contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="4740a-121">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="4740a-122">Эта ссылка на объект хранится в переменной с именем $context.</span><span class="sxs-lookup"><span data-stu-id="4740a-122">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="4740a-123">Затем вторая команда использует эту ссылку на объект и командлет **Disable-AzBatchComputeNodeScheduling** для подключения к пулу myPool и отключения планирования задач в узле tvm-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="4740a-123">The second command then uses this object reference and the **Disable-AzBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and disable task scheduling on node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="4740a-124">Так как *параметр DisableComputeNodeSchedulingOptions* не был включен в список задач, которые в данный момент запускаются на узле вычислений, будет выполняться повторно.</span><span class="sxs-lookup"><span data-stu-id="4740a-124">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute node will be requeued.</span></span>

### <span data-ttu-id="4740a-125">Пример 2. Отключение планирования задач на всех узлах компьютеров в пуле</span><span class="sxs-lookup"><span data-stu-id="4740a-125">Example 2: Disable task scheduling on all compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Disable-AzBatchComputeNodeScheduling -BatchContext $Context
```

<span data-ttu-id="4740a-126">Эти команды отключать планирование задач на всех узлах компьютеров в пакетном пуле пула.</span><span class="sxs-lookup"><span data-stu-id="4740a-126">These commands disable task scheduling on all the computer nodes in the batch pool Pool06.</span></span>
<span data-ttu-id="4740a-127">Для выполнения этой задачи первая команда в примере создает ссылку на ключи учетных записей для пакетной учетной записи contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="4740a-127">To perform this task, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="4740a-128">Эта ссылка на объект хранится в переменной с именем $context.</span><span class="sxs-lookup"><span data-stu-id="4740a-128">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="4740a-129">Вторая команда в этом примере использует эту ссылку на объект и **Get-AzBatchComputeNode** для получения коллекции всех узлов вычислений, найденных в Pool06.</span><span class="sxs-lookup"><span data-stu-id="4740a-129">The second command in the example then uses this object reference and **Get-AzBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="4740a-130">Затем эта коллекция передается в канал, чтобы отключить планирование задач на каждом узле вычислений в коллекции. </span><span class="sxs-lookup"><span data-stu-id="4740a-130">That collection is then piped to then **Disable-AzBatchComputeNodeScheduling** cmdlet to disable task scheduling on each compute node in the collection.</span></span>
<span data-ttu-id="4740a-131">Так как *параметр DisableComputeNodeSchedulingOptions* не был включен в список задач, которые в настоящее время будут выполняться на узлах компьютеров, будет выполняться повторно.</span><span class="sxs-lookup"><span data-stu-id="4740a-131">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute nodes will be requeued.</span></span>

## <span data-ttu-id="4740a-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4740a-132">PARAMETERS</span></span>

### <span data-ttu-id="4740a-133">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="4740a-133">-BatchContext</span></span>
<span data-ttu-id="4740a-134">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="4740a-134">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="4740a-135">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой batchy будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4740a-135">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="4740a-136">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="4740a-136">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="4740a-137">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4740a-137">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="4740a-138">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="4740a-138">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="4740a-139">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="4740a-139">-ComputeNode</span></span>
<span data-ttu-id="4740a-140">Указывает ссылку на узел вычислений, для которой отключено планирование задач.</span><span class="sxs-lookup"><span data-stu-id="4740a-140">Specifies an object reference to the compute node where task scheduling is disabled.</span></span>
<span data-ttu-id="4740a-141">Эта ссылка создается с помощью Get-AzBatchComputeNode и хранения возвращаемого объекта узла вычислений в переменной.</span><span class="sxs-lookup"><span data-stu-id="4740a-141">This object reference is created by using the Get-AzBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

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

### <span data-ttu-id="4740a-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4740a-142">-DefaultProfile</span></span>
<span data-ttu-id="4740a-143">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4740a-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4740a-144">-DisableSchedulingOption</span><span class="sxs-lookup"><span data-stu-id="4740a-144">-DisableSchedulingOption</span></span>
<span data-ttu-id="4740a-145">Определяет, как этот cmdlet работает с задачами, которые в данный момент запущены на узле компьютера, где планирование отключено.</span><span class="sxs-lookup"><span data-stu-id="4740a-145">Specifies how this cmdlet deals with any tasks currently running on the computer node where scheduling is being disabled.</span></span>
<span data-ttu-id="4740a-146">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="4740a-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4740a-147">"Просрочено".</span><span class="sxs-lookup"><span data-stu-id="4740a-147">Requeue.</span></span>
<span data-ttu-id="4740a-148">Задачи немедленно останавливаются и возвращаются в очередь заданий.</span><span class="sxs-lookup"><span data-stu-id="4740a-148">Tasks are stopped immediately and returned to the job queue.</span></span>
<span data-ttu-id="4740a-149">Это позволяет перепланировать задачи на другом узле компьютеров.</span><span class="sxs-lookup"><span data-stu-id="4740a-149">This enables the tasks to be rescheduled on another compute node.</span></span>
<span data-ttu-id="4740a-150">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4740a-150">This is the default value.</span></span> 
- <span data-ttu-id="4740a-151">Завершить.</span><span class="sxs-lookup"><span data-stu-id="4740a-151">Terminate.</span></span>
<span data-ttu-id="4740a-152">Задачи немедленно останавливаются и удаляются из очереди заданий.</span><span class="sxs-lookup"><span data-stu-id="4740a-152">Tasks are stopped immediately and removed from the job queue.</span></span>
<span data-ttu-id="4740a-153">Переплановка этих задач не планируется.</span><span class="sxs-lookup"><span data-stu-id="4740a-153">These tasks will not be rescheduled.</span></span> 
- <span data-ttu-id="4740a-154">"Простое задание задач".</span><span class="sxs-lookup"><span data-stu-id="4740a-154">TaskCompletion.</span></span>
<span data-ttu-id="4740a-155">Выполнение текущих задач можно выполнить до отключения планирования задач на узле вычислений.</span><span class="sxs-lookup"><span data-stu-id="4740a-155">Currently running tasks will be able to complete before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="4740a-156">Новые задачи не будут запланированы на этом узле.</span><span class="sxs-lookup"><span data-stu-id="4740a-156">No new tasks will be scheduled on this node.</span></span> 
- <span data-ttu-id="4740a-157">RetainedData.</span><span class="sxs-lookup"><span data-stu-id="4740a-157">RetainedData.</span></span>
<span data-ttu-id="4740a-158">В настоящий момент задачи завершаются, а срок хранения данных может истечь до отключения планирования задач на узле вычислений.</span><span class="sxs-lookup"><span data-stu-id="4740a-158">Currently running tasks will be able to complete and data retention periods will be able to expire before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="4740a-159">Новые задачи не будут запланированы на этом узле.</span><span class="sxs-lookup"><span data-stu-id="4740a-159">No new tasks will be scheduled on this node.</span></span>

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

### <span data-ttu-id="4740a-160">-Id</span><span class="sxs-lookup"><span data-stu-id="4740a-160">-Id</span></span>
<span data-ttu-id="4740a-161">Определяет ИД узла компьютеров, на котором отключено планирование задач.</span><span class="sxs-lookup"><span data-stu-id="4740a-161">Specifies the ID of the compute node where task scheduling is disabled.</span></span>

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

### <span data-ttu-id="4740a-162">-PoolId</span><span class="sxs-lookup"><span data-stu-id="4740a-162">-PoolId</span></span>
<span data-ttu-id="4740a-163">Определяет ИД пула пакетов, который содержит узел вычислений, для которых отключено планирование задач.</span><span class="sxs-lookup"><span data-stu-id="4740a-163">Specifies the ID of the batch pool that contains the compute node where task scheduling is disabled.</span></span>
<span data-ttu-id="4740a-164">Если вы используете параметр *PoolId,* не используйте его *в* той же команде.</span><span class="sxs-lookup"><span data-stu-id="4740a-164">If you use the *PoolId* parameter, do not use the *ComputeNode* parameter in that same command.</span></span>

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

### <span data-ttu-id="4740a-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4740a-165">CommonParameters</span></span>
<span data-ttu-id="4740a-166">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4740a-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4740a-167">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4740a-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4740a-168">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4740a-168">INPUTS</span></span>

### <span data-ttu-id="4740a-169">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="4740a-169">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="4740a-170">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4740a-170">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="4740a-171">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4740a-171">OUTPUTS</span></span>

### <span data-ttu-id="4740a-172">System.Void</span><span class="sxs-lookup"><span data-stu-id="4740a-172">System.Void</span></span>

## <span data-ttu-id="4740a-173">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4740a-173">NOTES</span></span>

## <span data-ttu-id="4740a-174">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4740a-174">RELATED LINKS</span></span>

[<span data-ttu-id="4740a-175">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="4740a-175">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="4740a-176">Enable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="4740a-176">Enable-AzBatchComputeNodeScheduling</span></span>](./Enable-AzBatchComputeNodeScheduling.md)


