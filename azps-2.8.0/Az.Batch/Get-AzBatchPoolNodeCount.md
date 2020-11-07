---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchpoolnodecount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolNodeCount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolNodeCount.md
ms.openlocfilehash: 0390e6f156e305c3ba5f34d78dcf33520098bee3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727700"
---
# <span data-ttu-id="9be9a-101">Get-AzBatchPoolNodeCount</span><span class="sxs-lookup"><span data-stu-id="9be9a-101">Get-AzBatchPoolNodeCount</span></span>

## <span data-ttu-id="9be9a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9be9a-102">SYNOPSIS</span></span>
<span data-ttu-id="9be9a-103">Возвращает количество узлов пакета для каждого состояния узла, сгруппированное по идентификатору пула.</span><span class="sxs-lookup"><span data-stu-id="9be9a-103">Gets Batch node counts per node state grouped by pool id.</span></span>

## <span data-ttu-id="9be9a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9be9a-104">SYNTAX</span></span>

### <span data-ttu-id="9be9a-105">AzureBatchPoolNodeCounts (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9be9a-105">AzureBatchPoolNodeCounts (Default)</span></span>
```
Get-AzBatchPoolNodeCount -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9be9a-106">PoolId</span><span class="sxs-lookup"><span data-stu-id="9be9a-106">PoolId</span></span>
```
Get-AzBatchPoolNodeCount [-PoolId <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9be9a-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="9be9a-107">ParentObject</span></span>
```
Get-AzBatchPoolNodeCount [-Pool <PSCloudPool>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9be9a-108">ODataFilter</span><span class="sxs-lookup"><span data-stu-id="9be9a-108">ODataFilter</span></span>
```
Get-AzBatchPoolNodeCount [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9be9a-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9be9a-109">DESCRIPTION</span></span>
<span data-ttu-id="9be9a-110">Командлет Get-AzBatchPoolNodeCount позволяет клиентам получать подсчитанные значения для каждого состояния узла, сгруппированного по пулам.</span><span class="sxs-lookup"><span data-stu-id="9be9a-110">The Get-AzBatchPoolNodeCount cmdlet allows customers to get back node counts per node state grouped by pool.</span></span> <span data-ttu-id="9be9a-111">Возможные состояния узлов: создание, ожидание, leavingPool, не в сети, прервано, перезагрузка, reimaging, запуск, запуск, startTaskFailed, неизвестный, непригодный для использования и waitingForStartTask.</span><span class="sxs-lookup"><span data-stu-id="9be9a-111">Possible node states are creating, idle, leavingPool, offline, preempted, rebooting, reimaging, running, starting, startTaskFailed, unknown, unusable and waitingForStartTask.</span></span> <span data-ttu-id="9be9a-112">Командлет принимает PoolId или параметр Pool для фильтрации только пула с указанным идентификатором пула.</span><span class="sxs-lookup"><span data-stu-id="9be9a-112">The cmdlet takes PoolId or Pool parameter to filter only pool with pool id specified.</span></span> 

## <span data-ttu-id="9be9a-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9be9a-113">EXAMPLES</span></span>

### <span data-ttu-id="9be9a-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9be9a-114">Example 1</span></span>

```powershell
PS C:\> $batchContext = Get-AzBatchAccountKeys -AccountName "contosobatch"
PS C:\> Get-AzBatchPoolNodeCount -BatchContext $batchContext

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0
contosopool2                   Idle: 1, Rebooting: 1, Total: 2                              Total: 0
```

<span data-ttu-id="9be9a-115">Перечень счетчиков узлов на каждом уровне узла для пулов в контексте учетной записи текущего пакета.</span><span class="sxs-lookup"><span data-stu-id="9be9a-115">List node counts per node state for pools under current batch account context.</span></span>

### <span data-ttu-id="9be9a-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9be9a-116">Example 2</span></span>

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

<span data-ttu-id="9be9a-117">Отображение счетчиков узлов на состояние узла для пула с указанным идентификатором.</span><span class="sxs-lookup"><span data-stu-id="9be9a-117">Show node counts per node state for a pool given pool id.</span></span>

## <span data-ttu-id="9be9a-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9be9a-118">PARAMETERS</span></span>

### <span data-ttu-id="9be9a-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="9be9a-119">-BatchContext</span></span>
<span data-ttu-id="9be9a-120">Экземпляр BatchAccountContext, который будет использоваться при взаимодействии со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="9be9a-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="9be9a-121">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="9be9a-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="9be9a-122">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="9be9a-122">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="9be9a-123">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="9be9a-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="9be9a-124">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="9be9a-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="9be9a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9be9a-125">-DefaultProfile</span></span>
<span data-ttu-id="9be9a-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9be9a-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9be9a-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="9be9a-127">-MaxCount</span></span>
<span data-ttu-id="9be9a-128">Задает максимальное количество возвращаемых пулов.</span><span class="sxs-lookup"><span data-stu-id="9be9a-128">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="9be9a-129">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="9be9a-129">The default value is 10.</span></span>

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

### <span data-ttu-id="9be9a-130">-Пул</span><span class="sxs-lookup"><span data-stu-id="9be9a-130">-Pool</span></span>
<span data-ttu-id="9be9a-131">Указывает **PSCloudPool** , для которого требуется получить количество узлов.</span><span class="sxs-lookup"><span data-stu-id="9be9a-131">Specifies the **PSCloudPool** for which to get node counts.</span></span>

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

### <span data-ttu-id="9be9a-132">-PoolId</span><span class="sxs-lookup"><span data-stu-id="9be9a-132">-PoolId</span></span>
<span data-ttu-id="9be9a-133">Идентификатор пула, для которого требуется получить количество узлов.</span><span class="sxs-lookup"><span data-stu-id="9be9a-133">The id of the pool for which to get node counts.</span></span>

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

### <span data-ttu-id="9be9a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9be9a-134">CommonParameters</span></span>
<span data-ttu-id="9be9a-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9be9a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9be9a-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9be9a-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9be9a-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9be9a-137">INPUTS</span></span>

### <span data-ttu-id="9be9a-138">System. String</span><span class="sxs-lookup"><span data-stu-id="9be9a-138">System.String</span></span>

### <span data-ttu-id="9be9a-139">Microsoft.Azure.Commands.BatCH. Models. PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="9be9a-139">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="9be9a-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="9be9a-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="9be9a-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9be9a-141">OUTPUTS</span></span>

### <span data-ttu-id="9be9a-142">Microsoft.Azure.Commands.BatCH. Models. PSPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="9be9a-142">Microsoft.Azure.Commands.Batch.Models.PSPoolNodeCounts</span></span>

## <span data-ttu-id="9be9a-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="9be9a-143">NOTES</span></span>

## <span data-ttu-id="9be9a-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9be9a-144">RELATED LINKS</span></span>

[<span data-ttu-id="9be9a-145">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="9be9a-145">Get-AzBatchAccountKeys</span></span>]()

[<span data-ttu-id="9be9a-146">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="9be9a-146">Get-AzBatchJob</span></span>]()

[<span data-ttu-id="9be9a-147">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="9be9a-147">Azure Batch Cmdlets</span></span>]()

