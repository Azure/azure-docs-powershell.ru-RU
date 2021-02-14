---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 93614655-A8F2-4A67-887D-43D41AB91F82
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchComputeNode.md
ms.openlocfilehash: a50329620944aa18458c3bb667e3a95ff45bc21f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100231188"
---
# <span data-ttu-id="18a0f-101">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="18a0f-101">Get-AzBatchComputeNode</span></span>

## <span data-ttu-id="18a0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18a0f-102">SYNOPSIS</span></span>
<span data-ttu-id="18a0f-103">Получает узлы пакетных вычислений из пула.</span><span class="sxs-lookup"><span data-stu-id="18a0f-103">Gets Batch compute nodes from a pool.</span></span>

## <span data-ttu-id="18a0f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="18a0f-104">SYNTAX</span></span>

### <span data-ttu-id="18a0f-105">ODataFilter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="18a0f-105">ODataFilter (Default)</span></span>
```
Get-AzBatchComputeNode [-PoolId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18a0f-106">ИД</span><span class="sxs-lookup"><span data-stu-id="18a0f-106">Id</span></span>
```
Get-AzBatchComputeNode [-PoolId] <String> [[-Id] <String>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18a0f-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="18a0f-107">ParentObject</span></span>
```
Get-AzBatchComputeNode [[-Pool] <PSCloudPool>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18a0f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="18a0f-108">DESCRIPTION</span></span>
<span data-ttu-id="18a0f-109">Для получения узлов обработки пакетных вычислений Azure из пула получается **cmdlet Get-AzBatchComputeNode.**</span><span class="sxs-lookup"><span data-stu-id="18a0f-109">The **Get-AzBatchComputeNode** cmdlet gets Azure Batch compute nodes from a pool.</span></span>
<span data-ttu-id="18a0f-110">Укажите параметр *PoolID* или *Pool.*</span><span class="sxs-lookup"><span data-stu-id="18a0f-110">Specify either the *PoolID* or *Pool* parameter.</span></span>
<span data-ttu-id="18a0f-111">Укажите *параметр "ИД",* чтобы получить один узел вычислений.</span><span class="sxs-lookup"><span data-stu-id="18a0f-111">Specify the *Id* parameter to get a single compute node.</span></span>
<span data-ttu-id="18a0f-112">Укажите *параметр Filter,* чтобы получить узлы компьютеров, которые соответствуют фильтру OData.</span><span class="sxs-lookup"><span data-stu-id="18a0f-112">Specify the *Filter* parameter to get the compute nodes that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="18a0f-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="18a0f-113">EXAMPLES</span></span>

### <span data-ttu-id="18a0f-114">Пример 1. Получить узел вычислений по ИД</span><span class="sxs-lookup"><span data-stu-id="18a0f-114">Example 1: Get a compute node by ID</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool06" -Id "tvm-2316545714_1-20150725t213220z" -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : standard_d1_v2
TotalTasksRun         : 1
StartTaskInformation  :
RecentTasks           : {}
StartTask             :
CertificateReferences :
Errors                :
```

<span data-ttu-id="18a0f-115">Эта команда получает узел вычислений, который содержит телевизор с ИД-2316545714_1-20150725t213220z из пула, который содержит ID Pool06.</span><span class="sxs-lookup"><span data-stu-id="18a0f-115">This command gets the compute node that has the ID tvm-2316545714_1-20150725t213220z from the pool that has the ID Pool06.</span></span>
<span data-ttu-id="18a0f-116">Используйте Get-AzBatchAccountKey для назначения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="18a0f-116">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="18a0f-117">Пример 2. Получить из пула все неавтовые узлы для компьютеров</span><span class="sxs-lookup"><span data-stu-id="18a0f-117">Example 2: Get all idle compute nodes from a pool</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool06" -Filter "state eq 'idle'" -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : standard_d1_v2
TotalTasksRun         : 1
StartTaskInformation  :
RecentTasks           : {}
StartTask             :
CertificateReferences :
Errors                :

Id                    : tvm-2316545714_2-20150726t172920z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_2-20150726t172920z
State                 : Idle
StateTransitionTime   : 7/26/2015 5:33:58 PM
LastBootTime          : 7/26/2015 5:33:58 PM
AllocationTime        : 7/26/2015 5:29:20 PM
IPAddress             : 10.14.121.38
AffinityId            : TVM:tvm-2316545714_2-20150726t172920z
VirtualMachineSize    : standard_d1_v2
TotalTasksRun         : 0
StartTaskInformation  :
RecentTasks           :
StartTask             :
CertificateReferences :
Errors                :
```

<span data-ttu-id="18a0f-118">Эта команда возвращает все узлы неательных компьютеров, содержащиеся в пуле с пулом ID Pool06.</span><span class="sxs-lookup"><span data-stu-id="18a0f-118">This command gets all idle compute nodes that are contained in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="18a0f-119">Команда определяет состояние неа установленного состояния с помощью *параметра Filter.*</span><span class="sxs-lookup"><span data-stu-id="18a0f-119">The command specifies the idle state by using the *Filter* parameter.</span></span>

### <span data-ttu-id="18a0f-120">Пример 3. Объединение всех узлов компьютеров в указанный пул</span><span class="sxs-lookup"><span data-stu-id="18a0f-120">Example 3: Get all compute nodes in a specified pool</span></span>
```
PS C:\>Get-AzBatchPool -Id "Pool07" -BatchContext $Context | Get-AzBatchComputeNode -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : standard_d1_v2
TotalTasksRun         : 1
StartTaskInformation  :
RecentTasks           : {}
StartTask             :
CertificateReferences :
Errors                :


Id                    : tvm-2316545714_2-20150726t172920z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_2-20150726t172920z
State                 : Idle
StateTransitionTime   : 7/26/2015 5:33:58 PM
LastBootTime          : 7/26/2015 5:33:58 PM
AllocationTime        : 7/26/2015 5:29:20 PM

IPAddress             : 10.14.121.38
AffinityId            : TVM:tvm-2316545714_2-20150726t172920z
VirtualMachineSize    : standard_d1_v2
TotalTasksRun         : 0
StartTaskInformation  :
RecentTasks           :
StartTask             :
CertificateReferences :
Errors                :
```

<span data-ttu-id="18a0f-121">Эта команда возвращает пул с пулом ID Pool07 с помощью Get-AzBatchPool командлета.</span><span class="sxs-lookup"><span data-stu-id="18a0f-121">This command gets the pool that has the ID Pool07 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="18a0f-122">Эта команда передает пул текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="18a0f-122">The command passes that pool to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="18a0f-123">Он получает все узлы компьютеров из этого пула.</span><span class="sxs-lookup"><span data-stu-id="18a0f-123">That cmdlet gets all compute nodes from that pool.</span></span>

## <span data-ttu-id="18a0f-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18a0f-124">PARAMETERS</span></span>

### <span data-ttu-id="18a0f-125">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="18a0f-125">-BatchContext</span></span>
<span data-ttu-id="18a0f-126">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="18a0f-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="18a0f-127">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой пакета будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="18a0f-127">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="18a0f-128">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="18a0f-128">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="18a0f-129">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="18a0f-129">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="18a0f-130">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="18a0f-130">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="18a0f-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18a0f-131">-DefaultProfile</span></span>
<span data-ttu-id="18a0f-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="18a0f-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18a0f-133">-Filter</span><span class="sxs-lookup"><span data-stu-id="18a0f-133">-Filter</span></span>
<span data-ttu-id="18a0f-134">Указывает предложение фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="18a0f-134">Specifies an OData filter clause.</span></span>
<span data-ttu-id="18a0f-135">Этот командлет возвращает вычислительные узлы, которые соответствуют фильтру, указанному этим параметром.</span><span class="sxs-lookup"><span data-stu-id="18a0f-135">This cmdlet returns compute nodes that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="18a0f-136">Если не указать фильтр, этот cmdlet возвращает все узлы компьютеров для пула.</span><span class="sxs-lookup"><span data-stu-id="18a0f-136">If you do not specify a filter, this cmdlet returns all compute nodes for the pool.</span></span>

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

### <span data-ttu-id="18a0f-137">-Id</span><span class="sxs-lookup"><span data-stu-id="18a0f-137">-Id</span></span>
<span data-ttu-id="18a0f-138">Определяет код узла вычислений, который этот cmdlet получает из пула.</span><span class="sxs-lookup"><span data-stu-id="18a0f-138">Specifies the ID of the compute node that this cmdlet gets from the pool.</span></span>
<span data-ttu-id="18a0f-139">Поддиавные знаки указывать нельзя.</span><span class="sxs-lookup"><span data-stu-id="18a0f-139">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18a0f-140">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="18a0f-140">-MaxCount</span></span>
<span data-ttu-id="18a0f-141">Указывает максимальное количество возвращаемых узлов компьютеров.</span><span class="sxs-lookup"><span data-stu-id="18a0f-141">Specifies the maximum number of compute nodes to return.</span></span>
<span data-ttu-id="18a0f-142">Если указать нулевое (ноль) или меньшее значение, для cmdlet не используется верхний предел.</span><span class="sxs-lookup"><span data-stu-id="18a0f-142">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="18a0f-143">Значение по умолчанию — 1000.</span><span class="sxs-lookup"><span data-stu-id="18a0f-143">The default value is 1000.</span></span>

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

### <span data-ttu-id="18a0f-144">-Pool</span><span class="sxs-lookup"><span data-stu-id="18a0f-144">-Pool</span></span>
<span data-ttu-id="18a0f-145">Пул (объект **PSCloudPool),** содержащий узлы для вычислений.</span><span class="sxs-lookup"><span data-stu-id="18a0f-145">Specifies the pool, as a **PSCloudPool** object, that contains the compute nodes.</span></span>
<span data-ttu-id="18a0f-146">Чтобы получить объект **PSCloudPool,** воспользуйтесь Get-AzBatchPool.</span><span class="sxs-lookup"><span data-stu-id="18a0f-146">To obtain a **PSCloudPool** object, use the Get-AzBatchPool cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudPool
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18a0f-147">-PoolId</span><span class="sxs-lookup"><span data-stu-id="18a0f-147">-PoolId</span></span>
<span data-ttu-id="18a0f-148">Определяет ИД пула, который содержит узлы для компьютеров.</span><span class="sxs-lookup"><span data-stu-id="18a0f-148">Specifies the ID of the pool that contains the compute nodes.</span></span>

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

### <span data-ttu-id="18a0f-149">-Select</span><span class="sxs-lookup"><span data-stu-id="18a0f-149">-Select</span></span>
<span data-ttu-id="18a0f-150">Указывает предложение выбора OData.</span><span class="sxs-lookup"><span data-stu-id="18a0f-150">Specifies an OData select clause.</span></span>
<span data-ttu-id="18a0f-151">Укажите значение этого параметра, чтобы получить определенные свойства, а не все свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="18a0f-151">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="18a0f-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18a0f-152">CommonParameters</span></span>
<span data-ttu-id="18a0f-153">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18a0f-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18a0f-154">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="18a0f-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18a0f-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="18a0f-155">INPUTS</span></span>

### <span data-ttu-id="18a0f-156">System.String</span><span class="sxs-lookup"><span data-stu-id="18a0f-156">System.String</span></span>

### <span data-ttu-id="18a0f-157">Microsoft.Azure.Commands.Batch. Models.PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="18a0f-157">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="18a0f-158">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="18a0f-158">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="18a0f-159">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="18a0f-159">OUTPUTS</span></span>

### <span data-ttu-id="18a0f-160">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="18a0f-160">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

## <span data-ttu-id="18a0f-161">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="18a0f-161">NOTES</span></span>

## <span data-ttu-id="18a0f-162">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="18a0f-162">RELATED LINKS</span></span>

[<span data-ttu-id="18a0f-163">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="18a0f-163">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="18a0f-164">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="18a0f-164">Get-AzBatchNodeFile</span></span>](./Get-AzBatchNodeFile.md)

[<span data-ttu-id="18a0f-165">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="18a0f-165">Get-AzBatchNodeFileContent</span></span>](./Get-AzBatchNodeFileContent.md)

[<span data-ttu-id="18a0f-166">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="18a0f-166">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="18a0f-167">Reset-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="18a0f-167">Reset-AzBatchComputeNode</span></span>](./Reset-AzBatchComputeNode.md)

[<span data-ttu-id="18a0f-168">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="18a0f-168">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)

[<span data-ttu-id="18a0f-169">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="18a0f-169">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
