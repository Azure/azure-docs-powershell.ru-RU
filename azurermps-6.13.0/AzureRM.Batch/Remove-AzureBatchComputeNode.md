---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 0BB79553-26DA-413C-8086-740DB6B31A85
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNode.md
ms.openlocfilehash: 39bbc9102d72c469730fe494869bffe5f726b41a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565914"
---
# <span data-ttu-id="95351-101">Remove-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="95351-101">Remove-AzureBatchComputeNode</span></span>

## <span data-ttu-id="95351-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="95351-102">SYNOPSIS</span></span>
<span data-ttu-id="95351-103">Удаляет из пула вычислительные узлы.</span><span class="sxs-lookup"><span data-stu-id="95351-103">Removes compute nodes from a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95351-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="95351-104">SYNTAX</span></span>

### <span data-ttu-id="95351-105">ID (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="95351-105">Id (Default)</span></span>
```
Remove-AzureBatchComputeNode [-PoolId] <String> [-Ids] <String[]>
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="95351-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="95351-106">InputObject</span></span>
```
Remove-AzureBatchComputeNode [[-ComputeNode] <PSComputeNode>]
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="95351-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="95351-107">DESCRIPTION</span></span>
<span data-ttu-id="95351-108">Командлет **Remove-AzureBatchComputeNode** удаляет пакетные вычисляемые узлы Azure из пула.</span><span class="sxs-lookup"><span data-stu-id="95351-108">The **Remove-AzureBatchComputeNode** cmdlet removes Azure Batch compute nodes from a pool.</span></span>

## <span data-ttu-id="95351-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="95351-109">EXAMPLES</span></span>

### <span data-ttu-id="95351-110">Пример 1: удаление вычислительного узла</span><span class="sxs-lookup"><span data-stu-id="95351-110">Example 1: Remove a compute node</span></span>
```
PS C:\>Remove-AzureBatchComputeNode -PoolId "Pool07" -Ids "tvm-2316545714_1-20150725t213220z" -DeallocationOption Terminate -ResizeTimeout ([TimeSpan]::FromMinutes(10)) -BatchContext $Context
```

<span data-ttu-id="95351-111">Эта команда удаляет узел COMPUTE node с указанным ИДЕНТИФИКАТОРом из пула с ИД Pool07.</span><span class="sxs-lookup"><span data-stu-id="95351-111">This command removes compute node that has the specified ID from pool that has the ID Pool07.</span></span>
<span data-ttu-id="95351-112">Команда задает параметр завершения освобождения.</span><span class="sxs-lookup"><span data-stu-id="95351-112">The command specifies the Terminate deallocation option.</span></span>
<span data-ttu-id="95351-113">Время ожидания изменения размера составляет 10 минут.</span><span class="sxs-lookup"><span data-stu-id="95351-113">The resize time-out is of 10 minutes.</span></span>

### <span data-ttu-id="95351-114">Пример 2: удаление вычислительного узла с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="95351-114">Example 2: Remove a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "Pool07" -Id "tvm-2316545714_1-20150725t213220z" -BatchContext $Context | Remove-AzureBatchComputeNode -Force -BatchContext $Context
```

<span data-ttu-id="95351-115">Эта команда получает вычислительный узел с указанным ИДЕНТИФИКАТОРом из пула с ИД Pool07 с помощью командлета Get-AzureBatchComputeNode.</span><span class="sxs-lookup"><span data-stu-id="95351-115">This command gets the compute node that has the specified ID from pool that has the ID Pool07 by using the Get-AzureBatchComputeNode cmdlet.</span></span>
<span data-ttu-id="95351-116">Команда передает этот узел текущему командлету с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="95351-116">The command passes that node to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="95351-117">Текущий командлет удаляет вычисляемый узел.</span><span class="sxs-lookup"><span data-stu-id="95351-117">The current cmdlet removes the compute node.</span></span>
<span data-ttu-id="95351-118">Команда задает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="95351-118">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="95351-119">Таким образом, команда не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="95351-119">Therefore, the command does not prompt you for confirmation.</span></span>

### <span data-ttu-id="95351-120">Пример 3: удаление нескольких узлов</span><span class="sxs-lookup"><span data-stu-id="95351-120">Example 3: Remove multiple nodes</span></span>
```
PS C:\>Remove-AzureBatchComputeNode -PoolId "Pool07" @("tvm-1783593343_28-20151117t214257z","tvm-1783593343_29-20151117t214257z") -Force -BatchContext $Context
```

<span data-ttu-id="95351-121">Эта команда удаляет два вычислительных узла из пула с ИД Pool07.</span><span class="sxs-lookup"><span data-stu-id="95351-121">This command removes two compute nodes from the pool that has the ID Pool07.</span></span>
<span data-ttu-id="95351-122">Команда не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="95351-122">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="95351-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="95351-123">PARAMETERS</span></span>

### <span data-ttu-id="95351-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="95351-124">-BatchContext</span></span>
<span data-ttu-id="95351-125">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="95351-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="95351-126">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="95351-126">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="95351-127">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="95351-127">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="95351-128">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="95351-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="95351-129">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="95351-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="95351-130">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="95351-130">-ComputeNode</span></span>
<span data-ttu-id="95351-131">Указывает объект **PSComputeNode** , представляющий вычислительный узел, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="95351-131">Specifies the **PSComputeNode** object that represents the compute node that this cmdlet removes.</span></span>

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

### <span data-ttu-id="95351-132">-DeallocationOption</span><span class="sxs-lookup"><span data-stu-id="95351-132">-DeallocationOption</span></span>
<span data-ttu-id="95351-133">Задает параметр освобождения для операции удаления, с которой начинается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="95351-133">Specifies a deallocation option for the removal operation that this cmdlet starts.</span></span>
<span data-ttu-id="95351-134">Значение по умолчанию — "очередь".</span><span class="sxs-lookup"><span data-stu-id="95351-134">The default value is Requeue.</span></span>

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

### <span data-ttu-id="95351-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95351-135">-DefaultProfile</span></span>
<span data-ttu-id="95351-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="95351-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95351-137">-Force</span><span class="sxs-lookup"><span data-stu-id="95351-137">-Force</span></span>
<span data-ttu-id="95351-138">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="95351-138">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="95351-139">-ID</span><span class="sxs-lookup"><span data-stu-id="95351-139">-Ids</span></span>
<span data-ttu-id="95351-140">Задает массив идентификаторов вычислительных узлов, которые этот командлет удаляет из пула.</span><span class="sxs-lookup"><span data-stu-id="95351-140">Specifies an array of IDs of compute nodes that this cmdlet removes from the pool.</span></span>

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

### <span data-ttu-id="95351-141">-PoolId</span><span class="sxs-lookup"><span data-stu-id="95351-141">-PoolId</span></span>
<span data-ttu-id="95351-142">Указывает идентификатор пула, который содержит вычислительные узлы, которые удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="95351-142">Specifies the ID of the pool that contains the compute nodes that this cmdlet removes.</span></span>

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

### <span data-ttu-id="95351-143">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="95351-143">-ResizeTimeout</span></span>
<span data-ttu-id="95351-144">Указывает интервал времени ожидания для удаления вычислительных узлов из пула.</span><span class="sxs-lookup"><span data-stu-id="95351-144">Specifies the time-out interval for removal of the compute nodes from the pool.</span></span>
<span data-ttu-id="95351-145">Значение по умолчанию — 10 минут.</span><span class="sxs-lookup"><span data-stu-id="95351-145">The default value is 10 minutes.</span></span>
<span data-ttu-id="95351-146">Минимальная величина составляет 5 минут.</span><span class="sxs-lookup"><span data-stu-id="95351-146">The minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="95351-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="95351-147">-Confirm</span></span>
<span data-ttu-id="95351-148">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="95351-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95351-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95351-149">-WhatIf</span></span>
<span data-ttu-id="95351-150">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="95351-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95351-151">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="95351-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95351-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95351-152">CommonParameters</span></span>
<span data-ttu-id="95351-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="95351-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95351-154">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95351-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95351-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="95351-155">INPUTS</span></span>

### <span data-ttu-id="95351-156">Microsoft.Azure.Commands.BatCH. Models. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="95351-156">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>
<span data-ttu-id="95351-157">Параметры: ComputeNode (ByValue)</span><span class="sxs-lookup"><span data-stu-id="95351-157">Parameters: ComputeNode (ByValue)</span></span>

### <span data-ttu-id="95351-158">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="95351-158">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="95351-159">Параметры: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="95351-159">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="95351-160">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="95351-160">OUTPUTS</span></span>

### <span data-ttu-id="95351-161">System. void</span><span class="sxs-lookup"><span data-stu-id="95351-161">System.Void</span></span>

## <span data-ttu-id="95351-162">Пуск</span><span class="sxs-lookup"><span data-stu-id="95351-162">NOTES</span></span>

## <span data-ttu-id="95351-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="95351-163">RELATED LINKS</span></span>

[<span data-ttu-id="95351-164">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="95351-164">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="95351-165">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="95351-165">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="95351-166">Restarting-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="95351-166">Restart-AzureBatchComputeNode</span></span>](./Restart-AzureBatchComputeNode.md)


