---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A202537B-D292-4822-A0B9-27A6A20621D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/reset-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Reset-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Reset-AzBatchComputeNode.md
ms.openlocfilehash: ff8c758b5e384fbab8f690030eb8a7fbe35c79f2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509586"
---
# <span data-ttu-id="cf10f-101">Reset-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="cf10f-101">Reset-AzBatchComputeNode</span></span>

## <span data-ttu-id="cf10f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf10f-102">SYNOPSIS</span></span>
<span data-ttu-id="cf10f-103">Переустановка операционной системы на указанном узле вычислений.</span><span class="sxs-lookup"><span data-stu-id="cf10f-103">Reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="cf10f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cf10f-104">SYNTAX</span></span>

### <span data-ttu-id="cf10f-105">ИД (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cf10f-105">Id (Default)</span></span>
```
Reset-AzBatchComputeNode [-PoolId] <String> [-Id] <String> [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf10f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="cf10f-106">InputObject</span></span>
```
Reset-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>] [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf10f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf10f-107">DESCRIPTION</span></span>
<span data-ttu-id="cf10f-108">**Cmdlet Reset-AzBatchComputeNode** переустановит операционную систему на указанном узле вычислений.</span><span class="sxs-lookup"><span data-stu-id="cf10f-108">The **Reset-AzBatchComputeNode** cmdlet reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="cf10f-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cf10f-109">EXAMPLES</span></span>

### <span data-ttu-id="cf10f-110">Пример 1. Повторное переимяние узла</span><span class="sxs-lookup"><span data-stu-id="cf10f-110">Example 1: Reimage a node</span></span>
```
PS C:\>Reset-AzBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="cf10f-111">Эта команда переимежает узел вычислений с помощью ИД "tvm-3257026573_2-20150813t200938z" в пуле MyPool.</span><span class="sxs-lookup"><span data-stu-id="cf10f-111">This command reimages the compute node with ID "tvm-3257026573_2-20150813t200938z" in the pool named MyPool.</span></span>
<span data-ttu-id="cf10f-112">Используйте Get-AzBatchAccountKey для назначения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="cf10f-112">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="cf10f-113">Пример 2. Повторное объединение всех узлов в пуле</span><span class="sxs-lookup"><span data-stu-id="cf10f-113">Example 2: Reimage all nodes in a pool</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Reset-AzBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="cf10f-114">Эта команда переимежает каждый узел вычислений в пуле MyPool.</span><span class="sxs-lookup"><span data-stu-id="cf10f-114">This command reimages every compute node in the pool named MyPool.</span></span>

## <span data-ttu-id="cf10f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf10f-115">PARAMETERS</span></span>

### <span data-ttu-id="cf10f-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="cf10f-116">-BatchContext</span></span>
<span data-ttu-id="cf10f-117">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="cf10f-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="cf10f-118">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой batchy будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cf10f-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="cf10f-119">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="cf10f-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="cf10f-120">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cf10f-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="cf10f-121">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="cf10f-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="cf10f-122">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="cf10f-122">-ComputeNode</span></span>
<span data-ttu-id="cf10f-123">Определяет объект **PSComputeNode,** который представляет узел вычислений, который нужно переимировать.</span><span class="sxs-lookup"><span data-stu-id="cf10f-123">Specifies the **PSComputeNode** object that represents the compute node to reimage.</span></span>

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

### <span data-ttu-id="cf10f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf10f-124">-DefaultProfile</span></span>
<span data-ttu-id="cf10f-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cf10f-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf10f-126">-Id</span><span class="sxs-lookup"><span data-stu-id="cf10f-126">-Id</span></span>
<span data-ttu-id="cf10f-127">Определяет ИД узла компьютеров, который нужно переинимировать.</span><span class="sxs-lookup"><span data-stu-id="cf10f-127">Specifies the ID of the compute node to reimage.</span></span>

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

### <span data-ttu-id="cf10f-128">-PoolId</span><span class="sxs-lookup"><span data-stu-id="cf10f-128">-PoolId</span></span>
<span data-ttu-id="cf10f-129">Определяет ИД пула, который содержит узел вычислений.</span><span class="sxs-lookup"><span data-stu-id="cf10f-129">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="cf10f-130">-ReimageOption</span><span class="sxs-lookup"><span data-stu-id="cf10f-130">-ReimageOption</span></span>
<span data-ttu-id="cf10f-131">Указывает, когда нужно повторное управление узлом и что делать с текущими задачами.</span><span class="sxs-lookup"><span data-stu-id="cf10f-131">Specifies when to reimage the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="cf10f-132">Значение по умолчанию — "Просрочено".</span><span class="sxs-lookup"><span data-stu-id="cf10f-132">The default is Requeue.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.ComputeNodeReimageOption]
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf10f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf10f-133">CommonParameters</span></span>
<span data-ttu-id="cf10f-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf10f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf10f-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cf10f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf10f-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cf10f-136">INPUTS</span></span>

### <span data-ttu-id="cf10f-137">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="cf10f-137">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="cf10f-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="cf10f-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="cf10f-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cf10f-139">OUTPUTS</span></span>

### <span data-ttu-id="cf10f-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="cf10f-140">System.Void</span></span>

## <span data-ttu-id="cf10f-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cf10f-141">NOTES</span></span>

## <span data-ttu-id="cf10f-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cf10f-142">RELATED LINKS</span></span>

[<span data-ttu-id="cf10f-143">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="cf10f-143">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="cf10f-144">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="cf10f-144">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)

[<span data-ttu-id="cf10f-145">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="cf10f-145">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
