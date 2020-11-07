---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2DF5FB4D-A5CB-439C-AC6F-DF2130AF33EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 9e93d6fd17d4ba308e6d5752554fb03639fce769
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912380"
---
# <span data-ttu-id="ba545-101">Disable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="ba545-101">Disable-AzBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="ba545-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ba545-102">SYNOPSIS</span></span>
<span data-ttu-id="ba545-103">Отключает планирование задач на заданном вычислительном узле.</span><span class="sxs-lookup"><span data-stu-id="ba545-103">Disables task scheduling on the specified compute node.</span></span>

## <span data-ttu-id="ba545-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ba545-104">SYNTAX</span></span>

### <span data-ttu-id="ba545-105">ID (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ba545-105">Id (Default)</span></span>
```
Disable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String>
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba545-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ba545-106">InputObject</span></span>
```
Disable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>]
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba545-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba545-107">DESCRIPTION</span></span>
<span data-ttu-id="ba545-108">Командлет **Disable-AzBatchComputeNodeScheduling** отключает планирование задач на заданном вычислительном узле.</span><span class="sxs-lookup"><span data-stu-id="ba545-108">The **Disable-AzBatchComputeNodeScheduling** cmdlet disables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="ba545-109">Вычислительный узел — это виртуальная машина Azure, выделенная для определенной рабочей нагрузки приложения.</span><span class="sxs-lookup"><span data-stu-id="ba545-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>
<span data-ttu-id="ba545-110">При отключении планирования задач на вычислительном узле вы также сможете определить, что делать в очереди задач узла.</span><span class="sxs-lookup"><span data-stu-id="ba545-110">When you disable task scheduling on a compute node you will also have the option of determining what to do about jobs currently in the node's task queue.</span></span>
<span data-ttu-id="ba545-111">**Disable-AzBatchComputeNodeScheduling** позволяет выполнять указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="ba545-111">**Disable-AzBatchComputeNodeScheduling** lets you do the following:</span></span> 
- <span data-ttu-id="ba545-112">Прервать задачи и вернуть их в очередь заданий.</span><span class="sxs-lookup"><span data-stu-id="ba545-112">Terminate the tasks and put them back in the job queue.</span></span>
<span data-ttu-id="ba545-113">Это позволяет перепланировать эти задачи на другом вычислительном узле.</span><span class="sxs-lookup"><span data-stu-id="ba545-113">This enables those tasks to be rescheduled on another compute node.</span></span> 
- <span data-ttu-id="ba545-114">Завершите задачи и удалите их из очереди заданий.</span><span class="sxs-lookup"><span data-stu-id="ba545-114">Terminate the tasks and remove them from the job queue.</span></span>
<span data-ttu-id="ba545-115">Задачи, остановленные таким образом, не будут перепланированы.</span><span class="sxs-lookup"><span data-stu-id="ba545-115">Tasks stopped in this manner will not be rescheduled.</span></span> 
- <span data-ttu-id="ba545-116">Дождитесь завершения всех задач, выполняемых в настоящее время, а затем отключите планирование задач на узле COMPUTE Node.</span><span class="sxs-lookup"><span data-stu-id="ba545-116">Wait for all the tasks currently being executed to complete and then disable task scheduling on the compute node.</span></span> 
- <span data-ttu-id="ba545-117">Дождитесь завершения всех выполняемых задач и истечения срока хранения данных, а затем отключите планирование задач на узле COMPUTE Node.</span><span class="sxs-lookup"><span data-stu-id="ba545-117">Wait for all the running tasks to complete and all the data retention periods to expire, and then disable task scheduling on the compute node.</span></span>

## <span data-ttu-id="ba545-118">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ba545-118">EXAMPLES</span></span>

### <span data-ttu-id="ba545-119">Пример 1: отключение планирования задач на вычислительном узле</span><span class="sxs-lookup"><span data-stu-id="ba545-119">Example 1: Disable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Disable-AzBatchComputeNodeScheduling -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="ba545-120">Эти команды отключают расписание задач на COMPUTE node TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="ba545-120">These commands disable task schedule on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="ba545-121">Для этого первой командой в примере создается ссылка на объект для contosobatchaccount учетной записи пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="ba545-121">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="ba545-122">Эта ссылка на объект хранится в переменной с именем $context.</span><span class="sxs-lookup"><span data-stu-id="ba545-122">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="ba545-123">Вторая команда использует эту ссылку на объект и командлет **Disable-AzBatchComputeNodeScheduling** для подключения к пулу myPool и отключения планирования задач на узле TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="ba545-123">The second command then uses this object reference and the **Disable-AzBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and disable task scheduling on node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="ba545-124">Так как параметр *DisableComputeNodeSchedulingOptions* не включал в себя все задачи, которые выполняются на вычислительном узле, они будут повторно помещены в очередь.</span><span class="sxs-lookup"><span data-stu-id="ba545-124">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute node will be requeued.</span></span>

### <span data-ttu-id="ba545-125">Пример 2: отключение планирования задач на всех вычислительных узлах в пуле</span><span class="sxs-lookup"><span data-stu-id="ba545-125">Example 2: Disable task scheduling on all compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Disable-AzBatchComputeNodeScheduling -BatchContext $Context
```

<span data-ttu-id="ba545-126">Эти команды отключают планирование задач на всех узлах компьютера в Pool06 пула пакетов.</span><span class="sxs-lookup"><span data-stu-id="ba545-126">These commands disable task scheduling on all the computer nodes in the batch pool Pool06.</span></span>
<span data-ttu-id="ba545-127">Для выполнения этой задачи в первой команде в примере создается ссылка на объект для учетной записи пакетной contosobatchaccount с помощью ключа учетной записи.</span><span class="sxs-lookup"><span data-stu-id="ba545-127">To perform this task, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="ba545-128">Эта ссылка на объект хранится в переменной с именем $context.</span><span class="sxs-lookup"><span data-stu-id="ba545-128">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="ba545-129">Во второй команде в примере используется ссылка на объект и **Get-AzBatchComputeNode** , чтобы вернуть коллекцию всех вычислительных узлов, обнаруженных в Pool06.</span><span class="sxs-lookup"><span data-stu-id="ba545-129">The second command in the example then uses this object reference and **Get-AzBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="ba545-130">После этого коллекция передается на командлет **Disable-AzBatchComputeNodeScheduling** , чтобы отключить планирование задач на каждом из вычислительных узлов коллекции.</span><span class="sxs-lookup"><span data-stu-id="ba545-130">That collection is then piped to then **Disable-AzBatchComputeNodeScheduling** cmdlet to disable task scheduling on each compute node in the collection.</span></span>
<span data-ttu-id="ba545-131">Так как параметр *DisableComputeNodeSchedulingOptions* не включал в себя все задачи, которые выполняются на вычислительных узлах, они будут повторно помещены в очередь.</span><span class="sxs-lookup"><span data-stu-id="ba545-131">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute nodes will be requeued.</span></span>

## <span data-ttu-id="ba545-132">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ba545-132">PARAMETERS</span></span>

### <span data-ttu-id="ba545-133">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ba545-133">-BatchContext</span></span>
<span data-ttu-id="ba545-134">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="ba545-134">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ba545-135">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="ba545-135">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ba545-136">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKey, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="ba545-136">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ba545-137">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="ba545-137">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ba545-138">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="ba545-138">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ba545-139">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="ba545-139">-ComputeNode</span></span>
<span data-ttu-id="ba545-140">Указывает ссылку на объект на вычислительный узел, если планирование задач отключено.</span><span class="sxs-lookup"><span data-stu-id="ba545-140">Specifies an object reference to the compute node where task scheduling is disabled.</span></span>
<span data-ttu-id="ba545-141">Эта ссылка на объект создается с помощью командлета Get-AzBatchComputeNode и сохраняет возвращаемый объект COMPUTE Node в переменной.</span><span class="sxs-lookup"><span data-stu-id="ba545-141">This object reference is created by using the Get-AzBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

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

### <span data-ttu-id="ba545-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba545-142">-DefaultProfile</span></span>
<span data-ttu-id="ba545-143">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ba545-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba545-144">-DisableSchedulingOption</span><span class="sxs-lookup"><span data-stu-id="ba545-144">-DisableSchedulingOption</span></span>
<span data-ttu-id="ba545-145">Указывает, как этот командлет обрабатывает все задачи, которые выполняются в данный момент на узле компьютера, где планирование отключено.</span><span class="sxs-lookup"><span data-stu-id="ba545-145">Specifies how this cmdlet deals with any tasks currently running on the computer node where scheduling is being disabled.</span></span>
<span data-ttu-id="ba545-146">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ba545-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ba545-147">Поочередно.</span><span class="sxs-lookup"><span data-stu-id="ba545-147">Requeue.</span></span>
<span data-ttu-id="ba545-148">Задачи немедленно останавливаются и возвращаются в очередь заданий.</span><span class="sxs-lookup"><span data-stu-id="ba545-148">Tasks are stopped immediately and returned to the job queue.</span></span>
<span data-ttu-id="ba545-149">Это позволяет перепланировать задачи на другом вычислительном узле.</span><span class="sxs-lookup"><span data-stu-id="ba545-149">This enables the tasks to be rescheduled on another compute node.</span></span>
<span data-ttu-id="ba545-150">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ba545-150">This is the default value.</span></span> 
- <span data-ttu-id="ba545-151">Разорван.</span><span class="sxs-lookup"><span data-stu-id="ba545-151">Terminate.</span></span>
<span data-ttu-id="ba545-152">Задачи немедленно останавливаются и удаляются из очереди заданий.</span><span class="sxs-lookup"><span data-stu-id="ba545-152">Tasks are stopped immediately and removed from the job queue.</span></span>
<span data-ttu-id="ba545-153">Эти задачи не будут перепланированы.</span><span class="sxs-lookup"><span data-stu-id="ba545-153">These tasks will not be rescheduled.</span></span> 
- <span data-ttu-id="ba545-154">TaskCompletion.</span><span class="sxs-lookup"><span data-stu-id="ba545-154">TaskCompletion.</span></span>
<span data-ttu-id="ba545-155">Запущенные в данный момент задачи можно выполнить, прежде чем планирование задач будет отключено на вычислительном узле.</span><span class="sxs-lookup"><span data-stu-id="ba545-155">Currently running tasks will be able to complete before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="ba545-156">На этом узле не будут планироваться новые задачи.</span><span class="sxs-lookup"><span data-stu-id="ba545-156">No new tasks will be scheduled on this node.</span></span> 
- <span data-ttu-id="ba545-157">RetainedData.</span><span class="sxs-lookup"><span data-stu-id="ba545-157">RetainedData.</span></span>
<span data-ttu-id="ba545-158">Запущенные в настоящее время задачи смогут завершить работу, и срок хранения данных будет ограничен, прежде чем планирование задач на узле COMPUTE node станет недоступным.</span><span class="sxs-lookup"><span data-stu-id="ba545-158">Currently running tasks will be able to complete and data retention periods will be able to expire before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="ba545-159">На этом узле не будут планироваться новые задачи.</span><span class="sxs-lookup"><span data-stu-id="ba545-159">No new tasks will be scheduled on this node.</span></span>

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

### <span data-ttu-id="ba545-160">-ID</span><span class="sxs-lookup"><span data-stu-id="ba545-160">-Id</span></span>
<span data-ttu-id="ba545-161">Указывает идентификатор вычислительного узла, на котором отключено планирование задач.</span><span class="sxs-lookup"><span data-stu-id="ba545-161">Specifies the ID of the compute node where task scheduling is disabled.</span></span>

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

### <span data-ttu-id="ba545-162">-PoolId</span><span class="sxs-lookup"><span data-stu-id="ba545-162">-PoolId</span></span>
<span data-ttu-id="ba545-163">Указывает идентификатор пула пакетов, содержащего вычислительный узел, для которого планирование задач отключено.</span><span class="sxs-lookup"><span data-stu-id="ba545-163">Specifies the ID of the batch pool that contains the compute node where task scheduling is disabled.</span></span>
<span data-ttu-id="ba545-164">Если вы используете параметр *PoolId* , не используйте параметр *ComputeNode* в той же команде.</span><span class="sxs-lookup"><span data-stu-id="ba545-164">If you use the *PoolId* parameter, do not use the *ComputeNode* parameter in that same command.</span></span>

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

### <span data-ttu-id="ba545-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba545-165">CommonParameters</span></span>
<span data-ttu-id="ba545-166">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ba545-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba545-167">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ba545-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba545-168">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ba545-168">INPUTS</span></span>

### <span data-ttu-id="ba545-169">Microsoft.Azure.Commands.BatCH. Models. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="ba545-169">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="ba545-170">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ba545-170">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="ba545-171">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba545-171">OUTPUTS</span></span>

### <span data-ttu-id="ba545-172">System. void</span><span class="sxs-lookup"><span data-stu-id="ba545-172">System.Void</span></span>

## <span data-ttu-id="ba545-173">Пуск</span><span class="sxs-lookup"><span data-stu-id="ba545-173">NOTES</span></span>

## <span data-ttu-id="ba545-174">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ba545-174">RELATED LINKS</span></span>

[<span data-ttu-id="ba545-175">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="ba545-175">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="ba545-176">Enable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="ba545-176">Enable-AzBatchComputeNodeScheduling</span></span>](./Enable-AzBatchComputeNodeScheduling.md)


