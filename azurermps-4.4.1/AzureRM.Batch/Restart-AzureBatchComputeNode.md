---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 029361F0-C4E9-4948-9EBA-BFBD1B029909
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Restart-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Restart-AzureBatchComputeNode.md
ms.openlocfilehash: eff141494c2b34622f35b687dd1803c449e8b727
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567175"
---
# <span data-ttu-id="5096f-101">Restart-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="5096f-101">Restart-AzureBatchComputeNode</span></span>

## <span data-ttu-id="5096f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5096f-102">SYNOPSIS</span></span>
<span data-ttu-id="5096f-103">Перезагружает указанный вычислительный узел.</span><span class="sxs-lookup"><span data-stu-id="5096f-103">Reboots the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5096f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5096f-104">SYNTAX</span></span>

### <span data-ttu-id="5096f-105">ID (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5096f-105">Id (Default)</span></span>
```
Restart-AzureBatchComputeNode [-PoolId] <String> [-Id] <String> [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5096f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="5096f-106">InputObject</span></span>
```
Restart-AzureBatchComputeNode [[-ComputeNode] <PSComputeNode>] [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5096f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5096f-107">DESCRIPTION</span></span>
<span data-ttu-id="5096f-108">Командлет **reboot-AzureBatchComputeNode** перезагружает указанный вычислительный узел.</span><span class="sxs-lookup"><span data-stu-id="5096f-108">The **Restart-AzureBatchComputeNode** cmdlet reboots the specified compute node.</span></span>

## <span data-ttu-id="5096f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5096f-109">EXAMPLES</span></span>

### <span data-ttu-id="5096f-110">Пример 1: перезапуск вычислительного узла</span><span class="sxs-lookup"><span data-stu-id="5096f-110">Example 1: Restart a compute node</span></span>
```
PS C:\>Restart-AzureBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="5096f-111">Эта команда перезагружает вычислительный узел с ИДЕНТИФИКАТОРом "TVM-3257026573_2-20150813t200938z" в пуле MyPool.</span><span class="sxs-lookup"><span data-stu-id="5096f-111">This command reboots the compute node with the ID "tvm-3257026573_2-20150813t200938z" in the pool MyPool.</span></span>

### <span data-ttu-id="5096f-112">Пример 2: Перезагрузите каждый вычислительный узел в пуле.</span><span class="sxs-lookup"><span data-stu-id="5096f-112">Example 2: Restart every compute node in a pool</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Restart-AzureBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="5096f-113">Эта команда перезагружает каждый вычислительный узел в пуле MyPool.</span><span class="sxs-lookup"><span data-stu-id="5096f-113">This command reboots every compute node in the pool MyPool.</span></span>

## <span data-ttu-id="5096f-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5096f-114">PARAMETERS</span></span>

### <span data-ttu-id="5096f-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="5096f-115">-BatchContext</span></span>
<span data-ttu-id="5096f-116">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="5096f-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5096f-117">Чтобы получить объект **BatchAccountContext** , содержащий клавиши доступа для вашей подписки, используйте командлет Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="5096f-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="5096f-118">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="5096f-118">-ComputeNode</span></span>
<span data-ttu-id="5096f-119">Указывает объект **PSComputeNode** , представляющий вычислительный узел для перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="5096f-119">Specifies the **PSComputeNode** object that represents the compute node to reboot.</span></span>

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

### <span data-ttu-id="5096f-120">-ID</span><span class="sxs-lookup"><span data-stu-id="5096f-120">-Id</span></span>
<span data-ttu-id="5096f-121">Указывает идентификатор вычислительного узла для перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="5096f-121">Specifies the ID of the compute node to reboot.</span></span>

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

### <span data-ttu-id="5096f-122">-PoolId</span><span class="sxs-lookup"><span data-stu-id="5096f-122">-PoolId</span></span>
<span data-ttu-id="5096f-123">Указывает идентификатор пула, который содержит вычислительный узел.</span><span class="sxs-lookup"><span data-stu-id="5096f-123">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="5096f-124">-RebootOption</span><span class="sxs-lookup"><span data-stu-id="5096f-124">-RebootOption</span></span>
<span data-ttu-id="5096f-125">Указывает, когда следует перезагружать узел и что делать с выполнением текущих задач.</span><span class="sxs-lookup"><span data-stu-id="5096f-125">Specifies when to reboot the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="5096f-126">По умолчанию используется очередь.</span><span class="sxs-lookup"><span data-stu-id="5096f-126">The default is Requeue.</span></span>

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

### <span data-ttu-id="5096f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5096f-127">-DefaultProfile</span></span>
<span data-ttu-id="5096f-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5096f-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5096f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5096f-129">CommonParameters</span></span>
<span data-ttu-id="5096f-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5096f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5096f-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5096f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5096f-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5096f-132">INPUTS</span></span>

### <span data-ttu-id="5096f-133">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5096f-133">BatchAccountContext</span></span>
<span data-ttu-id="5096f-134">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="5096f-134">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="5096f-135">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="5096f-135">PSComputeNode</span></span>
<span data-ttu-id="5096f-136">Параметр "ComputeNode" принимает значение типа "PSComputeNode" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="5096f-136">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="5096f-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5096f-137">OUTPUTS</span></span>

## <span data-ttu-id="5096f-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="5096f-138">NOTES</span></span>

## <span data-ttu-id="5096f-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5096f-139">RELATED LINKS</span></span>

[<span data-ttu-id="5096f-140">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="5096f-140">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="5096f-141">Сброс — AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="5096f-141">Reset-AzureBatchComputeNode</span></span>](./Reset-AzureBatchComputeNode.md)

[<span data-ttu-id="5096f-142">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="5096f-142">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


