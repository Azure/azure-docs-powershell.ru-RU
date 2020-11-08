---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A202537B-D292-4822-A0B9-27A6A20621D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/reset-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Reset-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Reset-AzBatchComputeNode.md
ms.openlocfilehash: a3342c80a2414727934c503818e400414f9bcaf2
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "94077177"
---
# <span data-ttu-id="3e74c-101">Reset-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="3e74c-101">Reset-AzBatchComputeNode</span></span>

## <span data-ttu-id="3e74c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3e74c-102">SYNOPSIS</span></span>
<span data-ttu-id="3e74c-103">Переустановка операционной системы на заданном вычислительном узле.</span><span class="sxs-lookup"><span data-stu-id="3e74c-103">Reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="3e74c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3e74c-104">SYNTAX</span></span>

### <span data-ttu-id="3e74c-105">ID (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3e74c-105">Id (Default)</span></span>
```
Reset-AzBatchComputeNode [-PoolId] <String> [-Id] <String> [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e74c-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="3e74c-106">InputObject</span></span>
```
Reset-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>] [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e74c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e74c-107">DESCRIPTION</span></span>
<span data-ttu-id="3e74c-108">Командлет **Reset-AzBatchComputeNode** переустанавливает операционную систему на заданном вычислительном узле.</span><span class="sxs-lookup"><span data-stu-id="3e74c-108">The **Reset-AzBatchComputeNode** cmdlet reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="3e74c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3e74c-109">EXAMPLES</span></span>

### <span data-ttu-id="3e74c-110">Пример 1: переизображение узла</span><span class="sxs-lookup"><span data-stu-id="3e74c-110">Example 1: Reimage a node</span></span>
```
PS C:\>Reset-AzBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="3e74c-111">Эта команда передается на узел COMPUTE node с ИДЕНТИФИКАТОРом "TVM-3257026573_2-20150813t200938z" в пуле с именем MyPool.</span><span class="sxs-lookup"><span data-stu-id="3e74c-111">This command reimages the compute node with ID "tvm-3257026573_2-20150813t200938z" in the pool named MyPool.</span></span>
<span data-ttu-id="3e74c-112">Используйте командлет Get-AzBatchAccountKey для присвоения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="3e74c-112">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="3e74c-113">Пример 2: переизображение всех узлов в пуле</span><span class="sxs-lookup"><span data-stu-id="3e74c-113">Example 2: Reimage all nodes in a pool</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Reset-AzBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="3e74c-114">Эта команда переобразует каждый вычислительный узел в пуле с именем MyPool.</span><span class="sxs-lookup"><span data-stu-id="3e74c-114">This command reimages every compute node in the pool named MyPool.</span></span>

## <span data-ttu-id="3e74c-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3e74c-115">PARAMETERS</span></span>

### <span data-ttu-id="3e74c-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="3e74c-116">-BatchContext</span></span>
<span data-ttu-id="3e74c-117">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="3e74c-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="3e74c-118">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="3e74c-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="3e74c-119">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKey, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="3e74c-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="3e74c-120">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="3e74c-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="3e74c-121">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="3e74c-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="3e74c-122">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="3e74c-122">-ComputeNode</span></span>
<span data-ttu-id="3e74c-123">Задает объект **PSComputeNode** , представляющий вычислительный узел для повторного изображения.</span><span class="sxs-lookup"><span data-stu-id="3e74c-123">Specifies the **PSComputeNode** object that represents the compute node to reimage.</span></span>

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

### <span data-ttu-id="3e74c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e74c-124">-DefaultProfile</span></span>
<span data-ttu-id="3e74c-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3e74c-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e74c-126">-ID</span><span class="sxs-lookup"><span data-stu-id="3e74c-126">-Id</span></span>
<span data-ttu-id="3e74c-127">Указывает идентификатор вычислительного узла для перезаписи изображений.</span><span class="sxs-lookup"><span data-stu-id="3e74c-127">Specifies the ID of the compute node to reimage.</span></span>

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

### <span data-ttu-id="3e74c-128">-PoolId</span><span class="sxs-lookup"><span data-stu-id="3e74c-128">-PoolId</span></span>
<span data-ttu-id="3e74c-129">Указывает идентификатор пула, который содержит вычислительный узел.</span><span class="sxs-lookup"><span data-stu-id="3e74c-129">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="3e74c-130">-ReimageOption</span><span class="sxs-lookup"><span data-stu-id="3e74c-130">-ReimageOption</span></span>
<span data-ttu-id="3e74c-131">Указывает, когда следует переобразировать узел и что делать с выполнением текущих задач.</span><span class="sxs-lookup"><span data-stu-id="3e74c-131">Specifies when to reimage the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="3e74c-132">По умолчанию используется очередь.</span><span class="sxs-lookup"><span data-stu-id="3e74c-132">The default is Requeue.</span></span>

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

### <span data-ttu-id="3e74c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e74c-133">CommonParameters</span></span>
<span data-ttu-id="3e74c-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3e74c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e74c-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e74c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e74c-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3e74c-136">INPUTS</span></span>

### <span data-ttu-id="3e74c-137">Microsoft.Azure.Commands.BatCH. Models. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="3e74c-137">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="3e74c-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="3e74c-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="3e74c-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e74c-139">OUTPUTS</span></span>

### <span data-ttu-id="3e74c-140">System. void</span><span class="sxs-lookup"><span data-stu-id="3e74c-140">System.Void</span></span>

## <span data-ttu-id="3e74c-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="3e74c-141">NOTES</span></span>

## <span data-ttu-id="3e74c-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3e74c-142">RELATED LINKS</span></span>

[<span data-ttu-id="3e74c-143">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="3e74c-143">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="3e74c-144">Restarting-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="3e74c-144">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)

[<span data-ttu-id="3e74c-145">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="3e74c-145">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


