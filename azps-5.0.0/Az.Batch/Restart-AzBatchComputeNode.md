---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 029361F0-C4E9-4948-9EBA-BFBD1B029909
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/restart-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Restart-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Restart-AzBatchComputeNode.md
ms.openlocfilehash: 41c6ea8e069e03a759c04f39018e2fa3a4d16834
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246420"
---
# <span data-ttu-id="3ab1d-101">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="3ab1d-101">Restart-AzBatchComputeNode</span></span>

## <span data-ttu-id="3ab1d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3ab1d-102">SYNOPSIS</span></span>
<span data-ttu-id="3ab1d-103">Перезагружает указанный вычислительный узел.</span><span class="sxs-lookup"><span data-stu-id="3ab1d-103">Reboots the specified compute node.</span></span>

## <span data-ttu-id="3ab1d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3ab1d-104">SYNTAX</span></span>

### <span data-ttu-id="3ab1d-105">ID (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3ab1d-105">Id (Default)</span></span>
```
Restart-AzBatchComputeNode [-PoolId] <String> [-Id] <String> [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ab1d-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="3ab1d-106">InputObject</span></span>
```
Restart-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>] [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ab1d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ab1d-107">DESCRIPTION</span></span>
<span data-ttu-id="3ab1d-108">Командлет **reboot-AzBatchComputeNode** перезагружает указанный вычислительный узел.</span><span class="sxs-lookup"><span data-stu-id="3ab1d-108">The **Restart-AzBatchComputeNode** cmdlet reboots the specified compute node.</span></span>

## <span data-ttu-id="3ab1d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3ab1d-109">EXAMPLES</span></span>

### <span data-ttu-id="3ab1d-110">Пример 1: перезапуск вычислительного узла</span><span class="sxs-lookup"><span data-stu-id="3ab1d-110">Example 1: Restart a compute node</span></span>
```
PS C:\>Restart-AzBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="3ab1d-111">Эта команда перезагружает вычислительный узел с ИДЕНТИФИКАТОРом "TVM-3257026573_2-20150813t200938z" в пуле MyPool.</span><span class="sxs-lookup"><span data-stu-id="3ab1d-111">This command reboots the compute node with the ID "tvm-3257026573_2-20150813t200938z" in the pool MyPool.</span></span>

### <span data-ttu-id="3ab1d-112">Пример 2: Перезагрузите каждый вычислительный узел в пуле.</span><span class="sxs-lookup"><span data-stu-id="3ab1d-112">Example 2: Restart every compute node in a pool</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Restart-AzBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="3ab1d-113">Эта команда перезагружает каждый вычислительный узел в пуле MyPool.</span><span class="sxs-lookup"><span data-stu-id="3ab1d-113">This command reboots every compute node in the pool MyPool.</span></span>

## <span data-ttu-id="3ab1d-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3ab1d-114">PARAMETERS</span></span>

### <span data-ttu-id="3ab1d-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="3ab1d-115">-BatchContext</span></span>
<span data-ttu-id="3ab1d-116">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="3ab1d-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="3ab1d-117">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="3ab1d-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="3ab1d-118">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKey, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="3ab1d-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="3ab1d-119">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="3ab1d-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="3ab1d-120">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="3ab1d-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="3ab1d-121">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="3ab1d-121">-ComputeNode</span></span>
<span data-ttu-id="3ab1d-122">Указывает объект **PSComputeNode** , представляющий вычислительный узел для перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="3ab1d-122">Specifies the **PSComputeNode** object that represents the compute node to reboot.</span></span>

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

### <span data-ttu-id="3ab1d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ab1d-123">-DefaultProfile</span></span>
<span data-ttu-id="3ab1d-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3ab1d-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ab1d-125">-ID</span><span class="sxs-lookup"><span data-stu-id="3ab1d-125">-Id</span></span>
<span data-ttu-id="3ab1d-126">Указывает идентификатор вычислительного узла для перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="3ab1d-126">Specifies the ID of the compute node to reboot.</span></span>

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

### <span data-ttu-id="3ab1d-127">-PoolId</span><span class="sxs-lookup"><span data-stu-id="3ab1d-127">-PoolId</span></span>
<span data-ttu-id="3ab1d-128">Указывает идентификатор пула, который содержит вычислительный узел.</span><span class="sxs-lookup"><span data-stu-id="3ab1d-128">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="3ab1d-129">-RebootOption</span><span class="sxs-lookup"><span data-stu-id="3ab1d-129">-RebootOption</span></span>
<span data-ttu-id="3ab1d-130">Указывает, когда следует перезагружать узел и что делать с выполнением текущих задач.</span><span class="sxs-lookup"><span data-stu-id="3ab1d-130">Specifies when to reboot the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="3ab1d-131">По умолчанию используется очередь.</span><span class="sxs-lookup"><span data-stu-id="3ab1d-131">The default is Requeue.</span></span>

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

### <span data-ttu-id="3ab1d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ab1d-132">CommonParameters</span></span>
<span data-ttu-id="3ab1d-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3ab1d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ab1d-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ab1d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ab1d-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3ab1d-135">INPUTS</span></span>

### <span data-ttu-id="3ab1d-136">Microsoft.Azure.Commands.BatCH. Models. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="3ab1d-136">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="3ab1d-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="3ab1d-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="3ab1d-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ab1d-138">OUTPUTS</span></span>

### <span data-ttu-id="3ab1d-139">System. void</span><span class="sxs-lookup"><span data-stu-id="3ab1d-139">System.Void</span></span>

## <span data-ttu-id="3ab1d-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="3ab1d-140">NOTES</span></span>

## <span data-ttu-id="3ab1d-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3ab1d-141">RELATED LINKS</span></span>

[<span data-ttu-id="3ab1d-142">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="3ab1d-142">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="3ab1d-143">Сброс — AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="3ab1d-143">Reset-AzBatchComputeNode</span></span>](./Reset-AzBatchComputeNode.md)

[<span data-ttu-id="3ab1d-144">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="3ab1d-144">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)