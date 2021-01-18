---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 029361F0-C4E9-4948-9EBA-BFBD1B029909
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/restart-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Restart-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Restart-AzBatchComputeNode.md
ms.openlocfilehash: 41c6ea8e069e03a759c04f39018e2fa3a4d16834
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509585"
---
# <span data-ttu-id="ecc9a-101">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="ecc9a-101">Restart-AzBatchComputeNode</span></span>

## <span data-ttu-id="ecc9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecc9a-102">SYNOPSIS</span></span>
<span data-ttu-id="ecc9a-103">Перезагружает указанный узел вычислений.</span><span class="sxs-lookup"><span data-stu-id="ecc9a-103">Reboots the specified compute node.</span></span>

## <span data-ttu-id="ecc9a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ecc9a-104">SYNTAX</span></span>

### <span data-ttu-id="ecc9a-105">ИД (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ecc9a-105">Id (Default)</span></span>
```
Restart-AzBatchComputeNode [-PoolId] <String> [-Id] <String> [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecc9a-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ecc9a-106">InputObject</span></span>
```
Restart-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>] [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecc9a-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ecc9a-107">DESCRIPTION</span></span>
<span data-ttu-id="ecc9a-108">Для **перезапуска azBatchComputeNode** перезагружается указанный узел вычислений.</span><span class="sxs-lookup"><span data-stu-id="ecc9a-108">The **Restart-AzBatchComputeNode** cmdlet reboots the specified compute node.</span></span>

## <span data-ttu-id="ecc9a-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ecc9a-109">EXAMPLES</span></span>

### <span data-ttu-id="ecc9a-110">Пример 1. Перезапуск узла вычислений</span><span class="sxs-lookup"><span data-stu-id="ecc9a-110">Example 1: Restart a compute node</span></span>
```
PS C:\>Restart-AzBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="ecc9a-111">Эта команда перезагружает узел вычислений с ИД "tvm-3257026573_2-20150813t200938z" в пуле MyPool.</span><span class="sxs-lookup"><span data-stu-id="ecc9a-111">This command reboots the compute node with the ID "tvm-3257026573_2-20150813t200938z" in the pool MyPool.</span></span>

### <span data-ttu-id="ecc9a-112">Пример 2. Перезапуск каждого узла вычислений в пуле</span><span class="sxs-lookup"><span data-stu-id="ecc9a-112">Example 2: Restart every compute node in a pool</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Restart-AzBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="ecc9a-113">Эта команда перезагружает все узлы компьютеров в пуле MyPool.</span><span class="sxs-lookup"><span data-stu-id="ecc9a-113">This command reboots every compute node in the pool MyPool.</span></span>

## <span data-ttu-id="ecc9a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ecc9a-114">PARAMETERS</span></span>

### <span data-ttu-id="ecc9a-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ecc9a-115">-BatchContext</span></span>
<span data-ttu-id="ecc9a-116">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="ecc9a-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ecc9a-117">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой пакета будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ecc9a-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ecc9a-118">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="ecc9a-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ecc9a-119">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ecc9a-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ecc9a-120">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="ecc9a-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ecc9a-121">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="ecc9a-121">-ComputeNode</span></span>
<span data-ttu-id="ecc9a-122">Определяет объект **PSComputeNode,** представляюрный узел вычислений, который нужно перезагрузить.</span><span class="sxs-lookup"><span data-stu-id="ecc9a-122">Specifies the **PSComputeNode** object that represents the compute node to reboot.</span></span>

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

### <span data-ttu-id="ecc9a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecc9a-123">-DefaultProfile</span></span>
<span data-ttu-id="ecc9a-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ecc9a-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ecc9a-125">-Id</span><span class="sxs-lookup"><span data-stu-id="ecc9a-125">-Id</span></span>
<span data-ttu-id="ecc9a-126">Определяет ИД узла компьютеров, который нужно перезагрузить.</span><span class="sxs-lookup"><span data-stu-id="ecc9a-126">Specifies the ID of the compute node to reboot.</span></span>

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

### <span data-ttu-id="ecc9a-127">-PoolId</span><span class="sxs-lookup"><span data-stu-id="ecc9a-127">-PoolId</span></span>
<span data-ttu-id="ecc9a-128">Определяет ИД пула, который содержит узел вычислений.</span><span class="sxs-lookup"><span data-stu-id="ecc9a-128">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="ecc9a-129">-RebootOption</span><span class="sxs-lookup"><span data-stu-id="ecc9a-129">-RebootOption</span></span>
<span data-ttu-id="ecc9a-130">Указывает, когда нужно перезагрузить узел и что делать с текущими задачами.</span><span class="sxs-lookup"><span data-stu-id="ecc9a-130">Specifies when to reboot the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="ecc9a-131">Значение по умолчанию — "Просрочено".</span><span class="sxs-lookup"><span data-stu-id="ecc9a-131">The default is Requeue.</span></span>

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

### <span data-ttu-id="ecc9a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecc9a-132">CommonParameters</span></span>
<span data-ttu-id="ecc9a-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecc9a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecc9a-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ecc9a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecc9a-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ecc9a-135">INPUTS</span></span>

### <span data-ttu-id="ecc9a-136">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="ecc9a-136">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="ecc9a-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ecc9a-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="ecc9a-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ecc9a-138">OUTPUTS</span></span>

### <span data-ttu-id="ecc9a-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="ecc9a-139">System.Void</span></span>

## <span data-ttu-id="ecc9a-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ecc9a-140">NOTES</span></span>

## <span data-ttu-id="ecc9a-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ecc9a-141">RELATED LINKS</span></span>

[<span data-ttu-id="ecc9a-142">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="ecc9a-142">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="ecc9a-143">Reset-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="ecc9a-143">Reset-AzBatchComputeNode</span></span>](./Reset-AzBatchComputeNode.md)

[<span data-ttu-id="ecc9a-144">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="ecc9a-144">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
