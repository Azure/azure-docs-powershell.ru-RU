---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 029361F0-C4E9-4948-9EBA-BFBD1B029909
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/restart-azurebatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Restart-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Restart-AzureBatchComputeNode.md
ms.openlocfilehash: 5f32963630769dc25ed62f47d93fe47e56abda91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563736"
---
# <span data-ttu-id="27d9c-101">Restart-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="27d9c-101">Restart-AzureBatchComputeNode</span></span>

## <span data-ttu-id="27d9c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="27d9c-102">SYNOPSIS</span></span>
<span data-ttu-id="27d9c-103">Перезагружает указанный вычислительный узел.</span><span class="sxs-lookup"><span data-stu-id="27d9c-103">Reboots the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27d9c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="27d9c-104">SYNTAX</span></span>

### <span data-ttu-id="27d9c-105">ID (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="27d9c-105">Id (Default)</span></span>
```
Restart-AzureBatchComputeNode [-PoolId] <String> [-Id] <String> [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27d9c-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="27d9c-106">InputObject</span></span>
```
Restart-AzureBatchComputeNode [[-ComputeNode] <PSComputeNode>] [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27d9c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="27d9c-107">DESCRIPTION</span></span>
<span data-ttu-id="27d9c-108">Командлет **reboot-AzureBatchComputeNode** перезагружает указанный вычислительный узел.</span><span class="sxs-lookup"><span data-stu-id="27d9c-108">The **Restart-AzureBatchComputeNode** cmdlet reboots the specified compute node.</span></span>

## <span data-ttu-id="27d9c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="27d9c-109">EXAMPLES</span></span>

### <span data-ttu-id="27d9c-110">Пример 1: перезапуск вычислительного узла</span><span class="sxs-lookup"><span data-stu-id="27d9c-110">Example 1: Restart a compute node</span></span>
```
PS C:\>Restart-AzureBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="27d9c-111">Эта команда перезагружает вычислительный узел с ИДЕНТИФИКАТОРом "TVM-3257026573_2-20150813t200938z" в пуле MyPool.</span><span class="sxs-lookup"><span data-stu-id="27d9c-111">This command reboots the compute node with the ID "tvm-3257026573_2-20150813t200938z" in the pool MyPool.</span></span>

### <span data-ttu-id="27d9c-112">Пример 2: Перезагрузите каждый вычислительный узел в пуле.</span><span class="sxs-lookup"><span data-stu-id="27d9c-112">Example 2: Restart every compute node in a pool</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Restart-AzureBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="27d9c-113">Эта команда перезагружает каждый вычислительный узел в пуле MyPool.</span><span class="sxs-lookup"><span data-stu-id="27d9c-113">This command reboots every compute node in the pool MyPool.</span></span>

## <span data-ttu-id="27d9c-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="27d9c-114">PARAMETERS</span></span>

### <span data-ttu-id="27d9c-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="27d9c-115">-BatchContext</span></span>
<span data-ttu-id="27d9c-116">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="27d9c-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="27d9c-117">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="27d9c-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="27d9c-118">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="27d9c-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="27d9c-119">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="27d9c-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="27d9c-120">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="27d9c-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="27d9c-121">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="27d9c-121">-ComputeNode</span></span>
<span data-ttu-id="27d9c-122">Указывает объект **PSComputeNode** , представляющий вычислительный узел для перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="27d9c-122">Specifies the **PSComputeNode** object that represents the compute node to reboot.</span></span>

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

### <span data-ttu-id="27d9c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27d9c-123">-DefaultProfile</span></span>
<span data-ttu-id="27d9c-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="27d9c-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27d9c-125">-ID</span><span class="sxs-lookup"><span data-stu-id="27d9c-125">-Id</span></span>
<span data-ttu-id="27d9c-126">Указывает идентификатор вычислительного узла для перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="27d9c-126">Specifies the ID of the compute node to reboot.</span></span>

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

### <span data-ttu-id="27d9c-127">-PoolId</span><span class="sxs-lookup"><span data-stu-id="27d9c-127">-PoolId</span></span>
<span data-ttu-id="27d9c-128">Указывает идентификатор пула, который содержит вычислительный узел.</span><span class="sxs-lookup"><span data-stu-id="27d9c-128">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="27d9c-129">-RebootOption</span><span class="sxs-lookup"><span data-stu-id="27d9c-129">-RebootOption</span></span>
<span data-ttu-id="27d9c-130">Указывает, когда следует перезагружать узел и что делать с выполнением текущих задач.</span><span class="sxs-lookup"><span data-stu-id="27d9c-130">Specifies when to reboot the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="27d9c-131">По умолчанию используется очередь.</span><span class="sxs-lookup"><span data-stu-id="27d9c-131">The default is Requeue.</span></span>

```yaml
Type: ComputeNodeRebootOption
Parameter Sets: (All)
Aliases: 
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27d9c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27d9c-132">CommonParameters</span></span>
<span data-ttu-id="27d9c-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="27d9c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27d9c-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27d9c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27d9c-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="27d9c-135">INPUTS</span></span>

### <span data-ttu-id="27d9c-136">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="27d9c-136">BatchAccountContext</span></span>
<span data-ttu-id="27d9c-137">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="27d9c-137">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="27d9c-138">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="27d9c-138">PSComputeNode</span></span>
<span data-ttu-id="27d9c-139">Параметр "ComputeNode" принимает значение типа "PSComputeNode" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="27d9c-139">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="27d9c-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="27d9c-140">OUTPUTS</span></span>

## <span data-ttu-id="27d9c-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="27d9c-141">NOTES</span></span>

## <span data-ttu-id="27d9c-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="27d9c-142">RELATED LINKS</span></span>

[<span data-ttu-id="27d9c-143">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="27d9c-143">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="27d9c-144">Сброс — AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="27d9c-144">Reset-AzureBatchComputeNode</span></span>](./Reset-AzureBatchComputeNode.md)

[<span data-ttu-id="27d9c-145">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="27d9c-145">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


