---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 0BB79553-26DA-413C-8086-740DB6B31A85
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNode.md
ms.openlocfilehash: 516d6baacbacb7cab7db590558074024396649a8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509602"
---
# <span data-ttu-id="07934-101">Remove-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="07934-101">Remove-AzBatchComputeNode</span></span>

## <span data-ttu-id="07934-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07934-102">SYNOPSIS</span></span>
<span data-ttu-id="07934-103">Удаляет вычислительные узлы из пула.</span><span class="sxs-lookup"><span data-stu-id="07934-103">Removes compute nodes from a pool.</span></span>

## <span data-ttu-id="07934-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="07934-104">SYNTAX</span></span>

### <span data-ttu-id="07934-105">ИД (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="07934-105">Id (Default)</span></span>
```
Remove-AzBatchComputeNode [-PoolId] <String> [-Ids] <String[]>
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="07934-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="07934-106">InputObject</span></span>
```
Remove-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>]
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="07934-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="07934-107">DESCRIPTION</span></span>
<span data-ttu-id="07934-108">Для **этого из пула удаляются** узлы пакетных вычислений Azure.</span><span class="sxs-lookup"><span data-stu-id="07934-108">The **Remove-AzBatchComputeNode** cmdlet removes Azure Batch compute nodes from a pool.</span></span>

## <span data-ttu-id="07934-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="07934-109">EXAMPLES</span></span>

### <span data-ttu-id="07934-110">Пример 1. Удаление узла для вычислений</span><span class="sxs-lookup"><span data-stu-id="07934-110">Example 1: Remove a compute node</span></span>
```
PS C:\>Remove-AzBatchComputeNode -PoolId "Pool07" -Ids "tvm-2316545714_1-20150725t213220z" -DeallocationOption Terminate -ResizeTimeout ([TimeSpan]::FromMinutes(10)) -BatchContext $Context
```

<span data-ttu-id="07934-111">Эта команда удаляет узел вычислений с указанным ИД из пула с пулом ID Pool07.</span><span class="sxs-lookup"><span data-stu-id="07934-111">This command removes compute node that has the specified ID from pool that has the ID Pool07.</span></span>
<span data-ttu-id="07934-112">Команда определяет параметр "Завершить поиск сделки".</span><span class="sxs-lookup"><span data-stu-id="07934-112">The command specifies the Terminate deallocation option.</span></span>
<span data-ttu-id="07934-113">Время простоя больше 10 минут.</span><span class="sxs-lookup"><span data-stu-id="07934-113">The resize time-out is of 10 minutes.</span></span>

### <span data-ttu-id="07934-114">Пример 2. Удаление узла вычислений с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="07934-114">Example 2: Remove a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool07" -Id "tvm-2316545714_1-20150725t213220z" -BatchContext $Context | Remove-AzBatchComputeNode -Force -BatchContext $Context
```

<span data-ttu-id="07934-115">Эта команда получает узел вычислений с указанным кодом из пула, который содержит пул ID07, с помощью Get-AzBatchComputeNode командлета.</span><span class="sxs-lookup"><span data-stu-id="07934-115">This command gets the compute node that has the specified ID from pool that has the ID Pool07 by using the Get-AzBatchComputeNode cmdlet.</span></span>
<span data-ttu-id="07934-116">Эта команда передает этот узел текущему командлету с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="07934-116">The command passes that node to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="07934-117">Текущий cmdlet удаляет узел вычислений.</span><span class="sxs-lookup"><span data-stu-id="07934-117">The current cmdlet removes the compute node.</span></span>
<span data-ttu-id="07934-118">Команда определяет параметр *Force.*</span><span class="sxs-lookup"><span data-stu-id="07934-118">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="07934-119">Таким образом, команда не будет запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="07934-119">Therefore, the command does not prompt you for confirmation.</span></span>

### <span data-ttu-id="07934-120">Пример 3. Удаление нескольких узлов</span><span class="sxs-lookup"><span data-stu-id="07934-120">Example 3: Remove multiple nodes</span></span>
```
PS C:\>Remove-AzBatchComputeNode -PoolId "Pool07" @("tvm-1783593343_28-20151117t214257z","tvm-1783593343_29-20151117t214257z") -Force -BatchContext $Context
```

<span data-ttu-id="07934-121">Эта команда удаляет два узла для вычислений из пула с пулом ID Pool07.</span><span class="sxs-lookup"><span data-stu-id="07934-121">This command removes two compute nodes from the pool that has the ID Pool07.</span></span>
<span data-ttu-id="07934-122">Команда не будет запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="07934-122">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="07934-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07934-123">PARAMETERS</span></span>

### <span data-ttu-id="07934-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="07934-124">-BatchContext</span></span>
<span data-ttu-id="07934-125">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="07934-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="07934-126">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой пакета будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="07934-126">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="07934-127">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="07934-127">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="07934-128">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="07934-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="07934-129">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="07934-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="07934-130">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="07934-130">-ComputeNode</span></span>
<span data-ttu-id="07934-131">Определяет объект **PSComputeNode,** представляюща узел вычислений, который удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07934-131">Specifies the **PSComputeNode** object that represents the compute node that this cmdlet removes.</span></span>

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

### <span data-ttu-id="07934-132">-DeallocationOption</span><span class="sxs-lookup"><span data-stu-id="07934-132">-DeallocationOption</span></span>
<span data-ttu-id="07934-133">Указывает способ размещения сделки для операции удаления, которая запускается этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07934-133">Specifies a deallocation option for the removal operation that this cmdlet starts.</span></span>
<span data-ttu-id="07934-134">Значение по умолчанию — "Просрочено".</span><span class="sxs-lookup"><span data-stu-id="07934-134">The default value is Requeue.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07934-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07934-135">-DefaultProfile</span></span>
<span data-ttu-id="07934-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="07934-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07934-137">-Force</span><span class="sxs-lookup"><span data-stu-id="07934-137">-Force</span></span>
<span data-ttu-id="07934-138">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="07934-138">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07934-139">-Ids</span><span class="sxs-lookup"><span data-stu-id="07934-139">-Ids</span></span>
<span data-ttu-id="07934-140">Определяет массив кодов узлов компьютеров, который этот cmdlet удаляет из пула.</span><span class="sxs-lookup"><span data-stu-id="07934-140">Specifies an array of IDs of compute nodes that this cmdlet removes from the pool.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Id
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07934-141">-PoolId</span><span class="sxs-lookup"><span data-stu-id="07934-141">-PoolId</span></span>
<span data-ttu-id="07934-142">Определяет код пула, который содержит узлы компьютеров, которые удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07934-142">Specifies the ID of the pool that contains the compute nodes that this cmdlet removes.</span></span>

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

### <span data-ttu-id="07934-143">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="07934-143">-ResizeTimeout</span></span>
<span data-ttu-id="07934-144">Определяет интервал времени, через который можно удалить узлы компьютеров из пула.</span><span class="sxs-lookup"><span data-stu-id="07934-144">Specifies the time-out interval for removal of the compute nodes from the pool.</span></span>
<span data-ttu-id="07934-145">Значение по умолчанию — 10 минут.</span><span class="sxs-lookup"><span data-stu-id="07934-145">The default value is 10 minutes.</span></span>
<span data-ttu-id="07934-146">Минимальное значение — 5 минут.</span><span class="sxs-lookup"><span data-stu-id="07934-146">The minimum value is 5 minutes.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07934-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="07934-147">-Confirm</span></span>
<span data-ttu-id="07934-148">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="07934-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07934-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07934-149">-WhatIf</span></span>
<span data-ttu-id="07934-150">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07934-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07934-151">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="07934-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07934-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07934-152">CommonParameters</span></span>
<span data-ttu-id="07934-153">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07934-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07934-154">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="07934-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07934-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="07934-155">INPUTS</span></span>

### <span data-ttu-id="07934-156">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="07934-156">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="07934-157">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="07934-157">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="07934-158">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="07934-158">OUTPUTS</span></span>

### <span data-ttu-id="07934-159">System.Void</span><span class="sxs-lookup"><span data-stu-id="07934-159">System.Void</span></span>

## <span data-ttu-id="07934-160">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="07934-160">NOTES</span></span>

## <span data-ttu-id="07934-161">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="07934-161">RELATED LINKS</span></span>

[<span data-ttu-id="07934-162">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="07934-162">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="07934-163">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="07934-163">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="07934-164">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="07934-164">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)


