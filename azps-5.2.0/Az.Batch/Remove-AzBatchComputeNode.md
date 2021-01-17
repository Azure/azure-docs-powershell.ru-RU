---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 0BB79553-26DA-413C-8086-740DB6B31A85
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNode.md
ms.openlocfilehash: 516d6baacbacb7cab7db590558074024396649a8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98408095"
---
# <span data-ttu-id="828d5-101">Remove-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="828d5-101">Remove-AzBatchComputeNode</span></span>

## <span data-ttu-id="828d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="828d5-102">SYNOPSIS</span></span>
<span data-ttu-id="828d5-103">Удаляет вычислительные узлы из пула.</span><span class="sxs-lookup"><span data-stu-id="828d5-103">Removes compute nodes from a pool.</span></span>

## <span data-ttu-id="828d5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="828d5-104">SYNTAX</span></span>

### <span data-ttu-id="828d5-105">ИД (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="828d5-105">Id (Default)</span></span>
```
Remove-AzBatchComputeNode [-PoolId] <String> [-Ids] <String[]>
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="828d5-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="828d5-106">InputObject</span></span>
```
Remove-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>]
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="828d5-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="828d5-107">DESCRIPTION</span></span>
<span data-ttu-id="828d5-108">Для **этого из пула удаляются** узлы пакетных вычислений Azure.</span><span class="sxs-lookup"><span data-stu-id="828d5-108">The **Remove-AzBatchComputeNode** cmdlet removes Azure Batch compute nodes from a pool.</span></span>

## <span data-ttu-id="828d5-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="828d5-109">EXAMPLES</span></span>

### <span data-ttu-id="828d5-110">Пример 1. Удаление узла для вычислений</span><span class="sxs-lookup"><span data-stu-id="828d5-110">Example 1: Remove a compute node</span></span>
```
PS C:\>Remove-AzBatchComputeNode -PoolId "Pool07" -Ids "tvm-2316545714_1-20150725t213220z" -DeallocationOption Terminate -ResizeTimeout ([TimeSpan]::FromMinutes(10)) -BatchContext $Context
```

<span data-ttu-id="828d5-111">Эта команда удаляет узел вычислений с указанным ИД из пула с пулом ID Pool07.</span><span class="sxs-lookup"><span data-stu-id="828d5-111">This command removes compute node that has the specified ID from pool that has the ID Pool07.</span></span>
<span data-ttu-id="828d5-112">Команда определяет параметр "Завершить поиск сделки".</span><span class="sxs-lookup"><span data-stu-id="828d5-112">The command specifies the Terminate deallocation option.</span></span>
<span data-ttu-id="828d5-113">Время простоя больше 10 минут.</span><span class="sxs-lookup"><span data-stu-id="828d5-113">The resize time-out is of 10 minutes.</span></span>

### <span data-ttu-id="828d5-114">Пример 2. Удаление узла вычислений с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="828d5-114">Example 2: Remove a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool07" -Id "tvm-2316545714_1-20150725t213220z" -BatchContext $Context | Remove-AzBatchComputeNode -Force -BatchContext $Context
```

<span data-ttu-id="828d5-115">Эта команда получает узел вычислений с указанным кодом из пула, который содержит пул ID07, с помощью Get-AzBatchComputeNode командлета.</span><span class="sxs-lookup"><span data-stu-id="828d5-115">This command gets the compute node that has the specified ID from pool that has the ID Pool07 by using the Get-AzBatchComputeNode cmdlet.</span></span>
<span data-ttu-id="828d5-116">Эта команда передает этот узел текущему командлету с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="828d5-116">The command passes that node to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="828d5-117">Текущий cmdlet удаляет узел вычислений.</span><span class="sxs-lookup"><span data-stu-id="828d5-117">The current cmdlet removes the compute node.</span></span>
<span data-ttu-id="828d5-118">Команда определяет параметр *Force.*</span><span class="sxs-lookup"><span data-stu-id="828d5-118">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="828d5-119">Таким образом, команда не будет запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="828d5-119">Therefore, the command does not prompt you for confirmation.</span></span>

### <span data-ttu-id="828d5-120">Пример 3. Удаление нескольких узлов</span><span class="sxs-lookup"><span data-stu-id="828d5-120">Example 3: Remove multiple nodes</span></span>
```
PS C:\>Remove-AzBatchComputeNode -PoolId "Pool07" @("tvm-1783593343_28-20151117t214257z","tvm-1783593343_29-20151117t214257z") -Force -BatchContext $Context
```

<span data-ttu-id="828d5-121">Эта команда удаляет два узла для вычислений из пула с пулом ID Pool07.</span><span class="sxs-lookup"><span data-stu-id="828d5-121">This command removes two compute nodes from the pool that has the ID Pool07.</span></span>
<span data-ttu-id="828d5-122">Команда не будет запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="828d5-122">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="828d5-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="828d5-123">PARAMETERS</span></span>

### <span data-ttu-id="828d5-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="828d5-124">-BatchContext</span></span>
<span data-ttu-id="828d5-125">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="828d5-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="828d5-126">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой пакета будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="828d5-126">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="828d5-127">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="828d5-127">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="828d5-128">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="828d5-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="828d5-129">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="828d5-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="828d5-130">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="828d5-130">-ComputeNode</span></span>
<span data-ttu-id="828d5-131">Определяет объект **PSComputeNode,** представляюща узел вычислений, который удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="828d5-131">Specifies the **PSComputeNode** object that represents the compute node that this cmdlet removes.</span></span>

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

### <span data-ttu-id="828d5-132">-DeallocationOption</span><span class="sxs-lookup"><span data-stu-id="828d5-132">-DeallocationOption</span></span>
<span data-ttu-id="828d5-133">Указывает способ размещения сделки для операции удаления, которая запускается этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="828d5-133">Specifies a deallocation option for the removal operation that this cmdlet starts.</span></span>
<span data-ttu-id="828d5-134">Значение по умолчанию — "Просрочено".</span><span class="sxs-lookup"><span data-stu-id="828d5-134">The default value is Requeue.</span></span>

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

### <span data-ttu-id="828d5-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="828d5-135">-DefaultProfile</span></span>
<span data-ttu-id="828d5-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="828d5-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="828d5-137">-Force</span><span class="sxs-lookup"><span data-stu-id="828d5-137">-Force</span></span>
<span data-ttu-id="828d5-138">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="828d5-138">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="828d5-139">-Ids</span><span class="sxs-lookup"><span data-stu-id="828d5-139">-Ids</span></span>
<span data-ttu-id="828d5-140">Определяет массив кодов узлов компьютеров, который этот cmdlet удаляет из пула.</span><span class="sxs-lookup"><span data-stu-id="828d5-140">Specifies an array of IDs of compute nodes that this cmdlet removes from the pool.</span></span>

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

### <span data-ttu-id="828d5-141">-PoolId</span><span class="sxs-lookup"><span data-stu-id="828d5-141">-PoolId</span></span>
<span data-ttu-id="828d5-142">Определяет код пула, который содержит узлы компьютеров, которые удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="828d5-142">Specifies the ID of the pool that contains the compute nodes that this cmdlet removes.</span></span>

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

### <span data-ttu-id="828d5-143">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="828d5-143">-ResizeTimeout</span></span>
<span data-ttu-id="828d5-144">Определяет интервал времени, через который можно удалить узлы компьютеров из пула.</span><span class="sxs-lookup"><span data-stu-id="828d5-144">Specifies the time-out interval for removal of the compute nodes from the pool.</span></span>
<span data-ttu-id="828d5-145">Значение по умолчанию — 10 минут.</span><span class="sxs-lookup"><span data-stu-id="828d5-145">The default value is 10 minutes.</span></span>
<span data-ttu-id="828d5-146">Минимальное значение — 5 минут.</span><span class="sxs-lookup"><span data-stu-id="828d5-146">The minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="828d5-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="828d5-147">-Confirm</span></span>
<span data-ttu-id="828d5-148">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="828d5-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="828d5-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="828d5-149">-WhatIf</span></span>
<span data-ttu-id="828d5-150">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="828d5-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="828d5-151">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="828d5-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="828d5-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="828d5-152">CommonParameters</span></span>
<span data-ttu-id="828d5-153">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="828d5-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="828d5-154">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="828d5-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="828d5-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="828d5-155">INPUTS</span></span>

### <span data-ttu-id="828d5-156">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="828d5-156">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="828d5-157">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="828d5-157">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="828d5-158">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="828d5-158">OUTPUTS</span></span>

### <span data-ttu-id="828d5-159">System.Void</span><span class="sxs-lookup"><span data-stu-id="828d5-159">System.Void</span></span>

## <span data-ttu-id="828d5-160">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="828d5-160">NOTES</span></span>

## <span data-ttu-id="828d5-161">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="828d5-161">RELATED LINKS</span></span>

[<span data-ttu-id="828d5-162">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="828d5-162">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="828d5-163">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="828d5-163">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="828d5-164">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="828d5-164">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)


