---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A202537B-D292-4822-A0B9-27A6A20621D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/reset-azurebatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Reset-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Reset-AzureBatchComputeNode.md
ms.openlocfilehash: 8e1fd78c51a6a41f1f455fc3672a0c340309f76c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734722"
---
# <span data-ttu-id="db5ad-101">Reset-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="db5ad-101">Reset-AzureBatchComputeNode</span></span>

## <span data-ttu-id="db5ad-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="db5ad-102">SYNOPSIS</span></span>
<span data-ttu-id="db5ad-103">Переустановка операционной системы на заданном вычислительном узле.</span><span class="sxs-lookup"><span data-stu-id="db5ad-103">Reinstalls the operating system on the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db5ad-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="db5ad-104">SYNTAX</span></span>

### <span data-ttu-id="db5ad-105">ID (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="db5ad-105">Id (Default)</span></span>
```
Reset-AzureBatchComputeNode [-PoolId] <String> [-Id] <String> [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db5ad-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="db5ad-106">InputObject</span></span>
```
Reset-AzureBatchComputeNode [[-ComputeNode] <PSComputeNode>] [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db5ad-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="db5ad-107">DESCRIPTION</span></span>
<span data-ttu-id="db5ad-108">Командлет **Reset-AzureBatchComputeNode** переустанавливает операционную систему на заданном вычислительном узле.</span><span class="sxs-lookup"><span data-stu-id="db5ad-108">The **Reset-AzureBatchComputeNode** cmdlet reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="db5ad-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="db5ad-109">EXAMPLES</span></span>

### <span data-ttu-id="db5ad-110">Пример 1: переизображение узла</span><span class="sxs-lookup"><span data-stu-id="db5ad-110">Example 1: Reimage a node</span></span>
```
PS C:\>Reset-AzureBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="db5ad-111">Эта команда передается на узел COMPUTE node с ИДЕНТИФИКАТОРом "TVM-3257026573_2-20150813t200938z" в пуле с именем MyPool.</span><span class="sxs-lookup"><span data-stu-id="db5ad-111">This command reimages the compute node with ID "tvm-3257026573_2-20150813t200938z" in the pool named MyPool.</span></span>
<span data-ttu-id="db5ad-112">Используйте командлет Get-AzureRmBatchAccountKeys для присвоения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="db5ad-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="db5ad-113">Пример 2: переизображение всех узлов в пуле</span><span class="sxs-lookup"><span data-stu-id="db5ad-113">Example 2: Reimage all nodes in a pool</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Reset-AzureBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="db5ad-114">Эта команда переобразует каждый вычислительный узел в пуле с именем MyPool.</span><span class="sxs-lookup"><span data-stu-id="db5ad-114">This command reimages every compute node in the pool named MyPool.</span></span>

## <span data-ttu-id="db5ad-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="db5ad-115">PARAMETERS</span></span>

### <span data-ttu-id="db5ad-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="db5ad-116">-BatchContext</span></span>
<span data-ttu-id="db5ad-117">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="db5ad-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="db5ad-118">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="db5ad-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="db5ad-119">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="db5ad-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="db5ad-120">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="db5ad-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="db5ad-121">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="db5ad-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db5ad-122">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="db5ad-122">-ComputeNode</span></span>
<span data-ttu-id="db5ad-123">Задает объект **PSComputeNode** , представляющий вычислительный узел для повторного изображения.</span><span class="sxs-lookup"><span data-stu-id="db5ad-123">Specifies the **PSComputeNode** object that represents the compute node to reimage.</span></span>

```yaml
Type: PSComputeNode
Parameter Sets: InputObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db5ad-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db5ad-124">-DefaultProfile</span></span>
<span data-ttu-id="db5ad-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="db5ad-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db5ad-126">-ID</span><span class="sxs-lookup"><span data-stu-id="db5ad-126">-Id</span></span>
<span data-ttu-id="db5ad-127">Указывает идентификатор вычислительного узла для перезаписи изображений.</span><span class="sxs-lookup"><span data-stu-id="db5ad-127">Specifies the ID of the compute node to reimage.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db5ad-128">-PoolId</span><span class="sxs-lookup"><span data-stu-id="db5ad-128">-PoolId</span></span>
<span data-ttu-id="db5ad-129">Указывает идентификатор пула, который содержит вычислительный узел.</span><span class="sxs-lookup"><span data-stu-id="db5ad-129">Specifies the ID of the pool that contains the compute node.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db5ad-130">-ReimageOption</span><span class="sxs-lookup"><span data-stu-id="db5ad-130">-ReimageOption</span></span>
<span data-ttu-id="db5ad-131">Указывает, когда следует переобразировать узел и что делать с выполнением текущих задач.</span><span class="sxs-lookup"><span data-stu-id="db5ad-131">Specifies when to reimage the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="db5ad-132">По умолчанию используется очередь.</span><span class="sxs-lookup"><span data-stu-id="db5ad-132">The default is Requeue.</span></span>

```yaml
Type: ComputeNodeReimageOption
Parameter Sets: (All)
Aliases: 
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db5ad-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db5ad-133">CommonParameters</span></span>
<span data-ttu-id="db5ad-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="db5ad-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db5ad-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db5ad-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db5ad-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="db5ad-136">INPUTS</span></span>

### <span data-ttu-id="db5ad-137">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="db5ad-137">BatchAccountContext</span></span>
<span data-ttu-id="db5ad-138">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="db5ad-138">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="db5ad-139">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="db5ad-139">PSComputeNode</span></span>
<span data-ttu-id="db5ad-140">Параметр "ComputeNode" принимает значение типа "PSComputeNode" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="db5ad-140">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="db5ad-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="db5ad-141">OUTPUTS</span></span>

## <span data-ttu-id="db5ad-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="db5ad-142">NOTES</span></span>

## <span data-ttu-id="db5ad-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="db5ad-143">RELATED LINKS</span></span>

[<span data-ttu-id="db5ad-144">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="db5ad-144">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="db5ad-145">Restarting-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="db5ad-145">Restart-AzureBatchComputeNode</span></span>](./Restart-AzureBatchComputeNode.md)

[<span data-ttu-id="db5ad-146">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="db5ad-146">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


