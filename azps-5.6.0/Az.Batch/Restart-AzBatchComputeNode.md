---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 029361F0-C4E9-4948-9EBA-BFBD1B029909
online version: https://docs.microsoft.com/powershell/module/az.batch/restart-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Restart-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Restart-AzBatchComputeNode.md
ms.openlocfilehash: daf89fec73ed18cf5b67c4100556d490795708d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985340"
---
# <span data-ttu-id="a8753-101">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="a8753-101">Restart-AzBatchComputeNode</span></span>

## <span data-ttu-id="a8753-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8753-102">SYNOPSIS</span></span>
<span data-ttu-id="a8753-103">Перезагружает указанный узел вычислений.</span><span class="sxs-lookup"><span data-stu-id="a8753-103">Reboots the specified compute node.</span></span>

## <span data-ttu-id="a8753-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a8753-104">SYNTAX</span></span>

### <span data-ttu-id="a8753-105">ИД (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a8753-105">Id (Default)</span></span>
```
Restart-AzBatchComputeNode [-PoolId] <String> [-Id] <String> [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8753-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a8753-106">InputObject</span></span>
```
Restart-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>] [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8753-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8753-107">DESCRIPTION</span></span>
<span data-ttu-id="a8753-108">Для **перезапуска azBatchComputeNode** перезагружается указанный узел вычислений.</span><span class="sxs-lookup"><span data-stu-id="a8753-108">The **Restart-AzBatchComputeNode** cmdlet reboots the specified compute node.</span></span>

## <span data-ttu-id="a8753-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a8753-109">EXAMPLES</span></span>

### <span data-ttu-id="a8753-110">Пример 1. Перезапуск узла вычислений</span><span class="sxs-lookup"><span data-stu-id="a8753-110">Example 1: Restart a compute node</span></span>
```
PS C:\>Restart-AzBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="a8753-111">Эта команда перезагружает узел вычислений с ИД "tvm-3257026573_2-20150813t200938z" в пуле MyPool.</span><span class="sxs-lookup"><span data-stu-id="a8753-111">This command reboots the compute node with the ID "tvm-3257026573_2-20150813t200938z" in the pool MyPool.</span></span>

### <span data-ttu-id="a8753-112">Пример 2. Перезапуск каждого узла вычислений в пуле</span><span class="sxs-lookup"><span data-stu-id="a8753-112">Example 2: Restart every compute node in a pool</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Restart-AzBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="a8753-113">Эта команда перезагружает все узлы компьютеров в пуле MyPool.</span><span class="sxs-lookup"><span data-stu-id="a8753-113">This command reboots every compute node in the pool MyPool.</span></span>

## <span data-ttu-id="a8753-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a8753-114">PARAMETERS</span></span>

### <span data-ttu-id="a8753-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a8753-115">-BatchContext</span></span>
<span data-ttu-id="a8753-116">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="a8753-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a8753-117">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой batchy будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a8753-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a8753-118">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="a8753-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a8753-119">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a8753-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a8753-120">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="a8753-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a8753-121">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="a8753-121">-ComputeNode</span></span>
<span data-ttu-id="a8753-122">Указывает объект **PSComputeNode,** представляюрный узел вычислений, который нужно перезагрузить.</span><span class="sxs-lookup"><span data-stu-id="a8753-122">Specifies the **PSComputeNode** object that represents the compute node to reboot.</span></span>

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

### <span data-ttu-id="a8753-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8753-123">-DefaultProfile</span></span>
<span data-ttu-id="a8753-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a8753-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8753-125">-Id</span><span class="sxs-lookup"><span data-stu-id="a8753-125">-Id</span></span>
<span data-ttu-id="a8753-126">Определяет ИД узла компьютеров, который нужно перезагрузить.</span><span class="sxs-lookup"><span data-stu-id="a8753-126">Specifies the ID of the compute node to reboot.</span></span>

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

### <span data-ttu-id="a8753-127">-PoolId</span><span class="sxs-lookup"><span data-stu-id="a8753-127">-PoolId</span></span>
<span data-ttu-id="a8753-128">Определяет ИД пула, который содержит узел вычислений.</span><span class="sxs-lookup"><span data-stu-id="a8753-128">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="a8753-129">-RebootOption</span><span class="sxs-lookup"><span data-stu-id="a8753-129">-RebootOption</span></span>
<span data-ttu-id="a8753-130">Указывает, когда нужно перезагрузить узел и что делать с текущими задачами.</span><span class="sxs-lookup"><span data-stu-id="a8753-130">Specifies when to reboot the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="a8753-131">Значение по умолчанию — "Просрочено".</span><span class="sxs-lookup"><span data-stu-id="a8753-131">The default is Requeue.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.ComputeNodeRebootOption]
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8753-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8753-132">CommonParameters</span></span>
<span data-ttu-id="a8753-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8753-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8753-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a8753-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8753-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a8753-135">INPUTS</span></span>

### <span data-ttu-id="a8753-136">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="a8753-136">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="a8753-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a8753-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="a8753-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a8753-138">OUTPUTS</span></span>

### <span data-ttu-id="a8753-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="a8753-139">System.Void</span></span>

## <span data-ttu-id="a8753-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a8753-140">NOTES</span></span>

## <span data-ttu-id="a8753-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a8753-141">RELATED LINKS</span></span>

[<span data-ttu-id="a8753-142">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="a8753-142">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="a8753-143">Reset-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="a8753-143">Reset-AzBatchComputeNode</span></span>](./Reset-AzBatchComputeNode.md)

[<span data-ttu-id="a8753-144">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="a8753-144">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
