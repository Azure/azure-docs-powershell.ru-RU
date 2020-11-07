---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A202537B-D292-4822-A0B9-27A6A20621D4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Reset-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Reset-AzureBatchComputeNode.md
ms.openlocfilehash: b90a70bb6b4a8104597056715c75f5699db5a24e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732882"
---
# <span data-ttu-id="cb121-101">Reset-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="cb121-101">Reset-AzureBatchComputeNode</span></span>

## <span data-ttu-id="cb121-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cb121-102">SYNOPSIS</span></span>
<span data-ttu-id="cb121-103">Переустановка операционной системы на заданном вычислительном узле.</span><span class="sxs-lookup"><span data-stu-id="cb121-103">Reinstalls the operating system on the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb121-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cb121-104">SYNTAX</span></span>

### <span data-ttu-id="cb121-105">ID (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cb121-105">Id (Default)</span></span>
```
Reset-AzureBatchComputeNode [-PoolId] <String> [-Id] <String> [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb121-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="cb121-106">InputObject</span></span>
```
Reset-AzureBatchComputeNode [[-ComputeNode] <PSComputeNode>] [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb121-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb121-107">DESCRIPTION</span></span>
<span data-ttu-id="cb121-108">Командлет **Reset-AzureBatchComputeNode** переустанавливает операционную систему на заданном вычислительном узле.</span><span class="sxs-lookup"><span data-stu-id="cb121-108">The **Reset-AzureBatchComputeNode** cmdlet reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="cb121-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cb121-109">EXAMPLES</span></span>

### <span data-ttu-id="cb121-110">Пример 1: переизображение узла</span><span class="sxs-lookup"><span data-stu-id="cb121-110">Example 1: Reimage a node</span></span>
```
PS C:\>Reset-AzureBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="cb121-111">Эта команда передается на узел COMPUTE node с ИДЕНТИФИКАТОРом "TVM-3257026573_2-20150813t200938z" в пуле с именем MyPool.</span><span class="sxs-lookup"><span data-stu-id="cb121-111">This command reimages the compute node with ID "tvm-3257026573_2-20150813t200938z" in the pool named MyPool.</span></span>
<span data-ttu-id="cb121-112">Используйте командлет Get-AzureRmBatchAccountKeys для присвоения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="cb121-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="cb121-113">Пример 2: переизображение всех узлов в пуле</span><span class="sxs-lookup"><span data-stu-id="cb121-113">Example 2: Reimage all nodes in a pool</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Reset-AzureBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="cb121-114">Эта команда переобразует каждый вычислительный узел в пуле с именем MyPool.</span><span class="sxs-lookup"><span data-stu-id="cb121-114">This command reimages every compute node in the pool named MyPool.</span></span>

## <span data-ttu-id="cb121-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cb121-115">PARAMETERS</span></span>

### <span data-ttu-id="cb121-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="cb121-116">-BatchContext</span></span>
<span data-ttu-id="cb121-117">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="cb121-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="cb121-118">Чтобы получить объект **BatchAccountContext** , содержащий клавиши доступа для вашей подписки, используйте командлет Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="cb121-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="cb121-119">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="cb121-119">-ComputeNode</span></span>
<span data-ttu-id="cb121-120">Задает объект **PSComputeNode** , представляющий вычислительный узел для повторного изображения.</span><span class="sxs-lookup"><span data-stu-id="cb121-120">Specifies the **PSComputeNode** object that represents the compute node to reimage.</span></span>

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

### <span data-ttu-id="cb121-121">-ID</span><span class="sxs-lookup"><span data-stu-id="cb121-121">-Id</span></span>
<span data-ttu-id="cb121-122">Указывает идентификатор вычислительного узла для перезаписи изображений.</span><span class="sxs-lookup"><span data-stu-id="cb121-122">Specifies the ID of the compute node to reimage.</span></span>

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

### <span data-ttu-id="cb121-123">-PoolId</span><span class="sxs-lookup"><span data-stu-id="cb121-123">-PoolId</span></span>
<span data-ttu-id="cb121-124">Указывает идентификатор пула, который содержит вычислительный узел.</span><span class="sxs-lookup"><span data-stu-id="cb121-124">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="cb121-125">-ReimageOption</span><span class="sxs-lookup"><span data-stu-id="cb121-125">-ReimageOption</span></span>
<span data-ttu-id="cb121-126">Указывает, когда следует переобразировать узел и что делать с выполнением текущих задач.</span><span class="sxs-lookup"><span data-stu-id="cb121-126">Specifies when to reimage the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="cb121-127">По умолчанию используется очередь.</span><span class="sxs-lookup"><span data-stu-id="cb121-127">The default is Requeue.</span></span>

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

### <span data-ttu-id="cb121-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb121-128">-DefaultProfile</span></span>
<span data-ttu-id="cb121-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cb121-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb121-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb121-130">CommonParameters</span></span>
<span data-ttu-id="cb121-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cb121-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb121-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb121-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb121-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cb121-133">INPUTS</span></span>

### <span data-ttu-id="cb121-134">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="cb121-134">BatchAccountContext</span></span>
<span data-ttu-id="cb121-135">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="cb121-135">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="cb121-136">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="cb121-136">PSComputeNode</span></span>
<span data-ttu-id="cb121-137">Параметр "ComputeNode" принимает значение типа "PSComputeNode" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="cb121-137">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="cb121-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb121-138">OUTPUTS</span></span>

## <span data-ttu-id="cb121-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="cb121-139">NOTES</span></span>

## <span data-ttu-id="cb121-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cb121-140">RELATED LINKS</span></span>

[<span data-ttu-id="cb121-141">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="cb121-141">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="cb121-142">Restarting-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="cb121-142">Restart-AzureBatchComputeNode</span></span>](./Restart-AzureBatchComputeNode.md)

[<span data-ttu-id="cb121-143">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="cb121-143">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


