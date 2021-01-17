---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchpoolnodecount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolNodeCount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolNodeCount.md
ms.openlocfilehash: b3b1adfe9549a7b04a1e7c6d57542cef8a40cfd7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396959"
---
# <span data-ttu-id="e5fd8-101">Get-AzBatchPoolNodeCount</span><span class="sxs-lookup"><span data-stu-id="e5fd8-101">Get-AzBatchPoolNodeCount</span></span>

## <span data-ttu-id="e5fd8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5fd8-102">SYNOPSIS</span></span>
<span data-ttu-id="e5fd8-103">Получает количество пакетных узлов для каждого состояния узла, сгруппировали по id пула.</span><span class="sxs-lookup"><span data-stu-id="e5fd8-103">Gets Batch node counts per node state grouped by pool id.</span></span>

## <span data-ttu-id="e5fd8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e5fd8-104">SYNTAX</span></span>

### <span data-ttu-id="e5fd8-105">AzureBatchPoolNodeCounts (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e5fd8-105">AzureBatchPoolNodeCounts (Default)</span></span>
```
Get-AzBatchPoolNodeCount -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e5fd8-106">PoolId</span><span class="sxs-lookup"><span data-stu-id="e5fd8-106">PoolId</span></span>
```
Get-AzBatchPoolNodeCount [-PoolId <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5fd8-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="e5fd8-107">ParentObject</span></span>
```
Get-AzBatchPoolNodeCount [-Pool <PSCloudPool>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5fd8-108">ODataFilter</span><span class="sxs-lookup"><span data-stu-id="e5fd8-108">ODataFilter</span></span>
```
Get-AzBatchPoolNodeCount [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5fd8-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5fd8-109">DESCRIPTION</span></span>
<span data-ttu-id="e5fd8-110">С Get-AzBatchPoolNodeCount позволяет клиентам возвращать количество узлов в каждого состояния узла, сгруппировали по пулу.</span><span class="sxs-lookup"><span data-stu-id="e5fd8-110">The Get-AzBatchPoolNodeCount cmdlet allows customers to get back node counts per node state grouped by pool.</span></span> <span data-ttu-id="e5fd8-111">Возможные состояния узла: создание, неактуальный, выход ИзPool, автономный, предустановленный, перезагрузка, перезагрузка, запуск, запуск, startTaskFailed, unknown, unusable и ожиданиеForStartTask.</span><span class="sxs-lookup"><span data-stu-id="e5fd8-111">Possible node states are creating, idle, leavingPool, offline, preempted, rebooting, reimaging, running, starting, startTaskFailed, unknown, unusable and waitingForStartTask.</span></span> <span data-ttu-id="e5fd8-112">Для фильтрации только пула с указанным ид пула для этого параметра принимается параметр PoolId или Pool.</span><span class="sxs-lookup"><span data-stu-id="e5fd8-112">The cmdlet takes PoolId or Pool parameter to filter only pool with pool id specified.</span></span> 

## <span data-ttu-id="e5fd8-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e5fd8-113">EXAMPLES</span></span>

### <span data-ttu-id="e5fd8-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e5fd8-114">Example 1</span></span>
```
PS C:\> $batchContext = Get-AzBatchAccountKey -AccountName "contosobatch"
PS C:\> Get-AzBatchPoolNodeCount -BatchContext $batchContext

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0
contosopool2                   Idle: 1, Rebooting: 1, Total: 2                              Total: 0
```

<span data-ttu-id="e5fd8-115">Узел списка подсчитываются в каждой области узла для пулов в контексте текущей пакетной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="e5fd8-115">List node counts per node state for pools under current batch account context.</span></span>

### <span data-ttu-id="e5fd8-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e5fd8-116">Example 2</span></span>

```powershell
PS C:\> Get-AzBatchPoolNodeCount -BatchContext $batchContext -PoolId "contosopool1"

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0

PS C:\> $poolnodecounts = Get-AzBatchPoolNodeCount -BatchContext $batchContext -PoolId "contosopool1"
PS C:\> $poolnodecounts.Dedicated

Creating            : 1
Idle                : 1
LeavingPool         : 0
Offline             : 0
Preempted           : 0
Rebooting           : 1
Reimaging           : 0
Running             : 5
Starting            : 0
StartTaskFailed     : 0
Total               : 8
Unknown             : 0
Unusable            : 0
WaitingForStartTask : 0

PS C:\> Get-AzBatchPool -Id "contosopool1" -BatchContext $batchContext | Get-AzBatchPoolNodeCount -BatchContext $batchContext

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0
```

<span data-ttu-id="e5fd8-117">Показывать количество узлов в состоянии узла для заданного пула.</span><span class="sxs-lookup"><span data-stu-id="e5fd8-117">Show node counts per node state for a pool given pool id.</span></span>

## <span data-ttu-id="e5fd8-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5fd8-118">PARAMETERS</span></span>

### <span data-ttu-id="e5fd8-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e5fd8-119">-BatchContext</span></span>
<span data-ttu-id="e5fd8-120">Экземпляр BatchAccountContext, который используется при взаимодействии со службой batch.</span><span class="sxs-lookup"><span data-stu-id="e5fd8-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="e5fd8-121">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой пакета будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e5fd8-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="e5fd8-122">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="e5fd8-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="e5fd8-123">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e5fd8-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="e5fd8-124">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="e5fd8-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e5fd8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5fd8-125">-DefaultProfile</span></span>
<span data-ttu-id="e5fd8-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e5fd8-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5fd8-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="e5fd8-127">-MaxCount</span></span>
<span data-ttu-id="e5fd8-128">Указывает максимальное количество пулов, которые нужно вернуть.</span><span class="sxs-lookup"><span data-stu-id="e5fd8-128">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="e5fd8-129">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="e5fd8-129">The default value is 10.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5fd8-130">-Pool</span><span class="sxs-lookup"><span data-stu-id="e5fd8-130">-Pool</span></span>
<span data-ttu-id="e5fd8-131">Определяет **PSCloudPool,** для которого нужно подсчитать количество узлов.</span><span class="sxs-lookup"><span data-stu-id="e5fd8-131">Specifies the **PSCloudPool** for which to get node counts.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudPool
Parameter Sets: ParentObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5fd8-132">-PoolId</span><span class="sxs-lookup"><span data-stu-id="e5fd8-132">-PoolId</span></span>
<span data-ttu-id="e5fd8-133">Id пула, для которого требуется подсчитать количество узлов.</span><span class="sxs-lookup"><span data-stu-id="e5fd8-133">The id of the pool for which to get node counts.</span></span>

```yaml
Type: System.String
Parameter Sets: PoolId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5fd8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5fd8-134">CommonParameters</span></span>
<span data-ttu-id="e5fd8-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5fd8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5fd8-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e5fd8-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5fd8-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e5fd8-137">INPUTS</span></span>

### <span data-ttu-id="e5fd8-138">System.String</span><span class="sxs-lookup"><span data-stu-id="e5fd8-138">System.String</span></span>

### <span data-ttu-id="e5fd8-139">Microsoft.Azure.Commands.Batch. Models.PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="e5fd8-139">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="e5fd8-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e5fd8-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e5fd8-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e5fd8-141">OUTPUTS</span></span>

### <span data-ttu-id="e5fd8-142">Microsoft.Azure.Commands.Batch. Models.PSPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="e5fd8-142">Microsoft.Azure.Commands.Batch.Models.PSPoolNodeCounts</span></span>

## <span data-ttu-id="e5fd8-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e5fd8-143">NOTES</span></span>

## <span data-ttu-id="e5fd8-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e5fd8-144">RELATED LINKS</span></span>

[<span data-ttu-id="e5fd8-145">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="e5fd8-145">Get-AzBatchAccountKey</span></span>]()

[<span data-ttu-id="e5fd8-146">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="e5fd8-146">Get-AzBatchJob</span></span>]()

[<span data-ttu-id="e5fd8-147">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="e5fd8-147">Azure Batch Cmdlets</span></span>]()

