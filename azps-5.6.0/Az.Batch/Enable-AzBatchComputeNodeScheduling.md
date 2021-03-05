---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 36EB9CE6-EAC9-471C-97D6-14E882E0F710
online version: https://docs.microsoft.com/powershell/module/az.batch/enable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 2897a21f25ac0a91fec11d83b77c8219d12f88ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995725"
---
# <span data-ttu-id="1270c-101">Enable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="1270c-101">Enable-AzBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="1270c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1270c-102">SYNOPSIS</span></span>
<span data-ttu-id="1270c-103">Включает планирование задач для указанного узла вычислений.</span><span class="sxs-lookup"><span data-stu-id="1270c-103">Enables task scheduling on the specified compute node.</span></span>

## <span data-ttu-id="1270c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1270c-104">SYNTAX</span></span>

### <span data-ttu-id="1270c-105">ИД (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1270c-105">Id (Default)</span></span>
```
Enable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1270c-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="1270c-106">InputObject</span></span>
```
Enable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1270c-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1270c-107">DESCRIPTION</span></span>
<span data-ttu-id="1270c-108">С **помощью cmdlet Enable-AzBatchComputeNodeScheduling** можно запланировать задачи для указанного узла вычислений.</span><span class="sxs-lookup"><span data-stu-id="1270c-108">The **Enable-AzBatchComputeNodeScheduling** cmdlet enables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="1270c-109">Узел вычислений — это виртуальная машинка Azure, предназначенная для конкретной рабочей нагрузки приложения.</span><span class="sxs-lookup"><span data-stu-id="1270c-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>

## <span data-ttu-id="1270c-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1270c-110">EXAMPLES</span></span>

### <span data-ttu-id="1270c-111">Пример 1. Включить планирование задач на узле вычислений</span><span class="sxs-lookup"><span data-stu-id="1270c-111">Example 1: Enable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Enable-AzBatchComputeNodeScheduling  -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="1270c-112">Эти команды позволяют планирование задач на узле вычислений tvm-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="1270c-112">These commands enable task scheduling on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="1270c-113">Для этого первая команда из примера создает ссылку на объект, содержащую ключи учетных записей для пакетной учетной записи contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="1270c-113">To do this, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="1270c-114">Эта ссылка на объект хранится в переменной с именем $context.</span><span class="sxs-lookup"><span data-stu-id="1270c-114">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="1270c-115">Затем вторая команда использует эту ссылку на объект и командлет **Enable-AzBatchComputeNodeScheduling** для подключения к пулу myPool и включить планирование задач в твм-1783593343_34-2015117t222514z.</span><span class="sxs-lookup"><span data-stu-id="1270c-115">The second command then uses this object reference and the **Enable-AzBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and enable task scheduling on tvm-1783593343_34-20151117t222514z.</span></span>

### <span data-ttu-id="1270c-116">Пример 2. Включить планирование задач на узлах компьютеров в пуле</span><span class="sxs-lookup"><span data-stu-id="1270c-116">Example 2: Enable task scheduling on compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Enable-AzBatchComputeNodeScheduling  -BatchContext $Context
```

<span data-ttu-id="1270c-117">Эти команды позволяют запланировать задачи на всех вычислительных узлах в пуле пула.</span><span class="sxs-lookup"><span data-stu-id="1270c-117">These commands enable task scheduling on all the compute nodes found in the pool Pool06.</span></span>
<span data-ttu-id="1270c-118">Для выполнения этой задачи первая команда из примера создает ссылку на объект, содержащую ключи учетной записи для пакетной учетной записи contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="1270c-118">To perform this task, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="1270c-119">Эта ссылка на объект хранится в переменной с именем $context.</span><span class="sxs-lookup"><span data-stu-id="1270c-119">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="1270c-120">Вторая команда в этом примере использует эту ссылку на объект и **Get-AzBatchComputeNode** для получения коллекции всех узлов вычислений, найденных в Pool06.</span><span class="sxs-lookup"><span data-stu-id="1270c-120">The second command in the example then uses this object reference and **Get-AzBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="1270c-121">Затем эта коллекция передается в канал **Enable-AzBatchComputeNodeScheduling,** который обеспечивает планирование задач для каждого узла вычислений в коллекции.</span><span class="sxs-lookup"><span data-stu-id="1270c-121">That collection is then piped to the **Enable-AzBatchComputeNodeScheduling** cmdlet, which enables task scheduling on each compute node in the collection.</span></span>

## <span data-ttu-id="1270c-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1270c-122">PARAMETERS</span></span>

### <span data-ttu-id="1270c-123">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="1270c-123">-BatchContext</span></span>
<span data-ttu-id="1270c-124">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="1270c-124">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="1270c-125">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой batchy будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1270c-125">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="1270c-126">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="1270c-126">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="1270c-127">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1270c-127">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="1270c-128">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="1270c-128">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="1270c-129">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="1270c-129">-ComputeNode</span></span>
<span data-ttu-id="1270c-130">Указывает ссылку на узел вычислений, на котором включено планирование задач.</span><span class="sxs-lookup"><span data-stu-id="1270c-130">Specifies an object reference to the compute node where task scheduling is enabled.</span></span>
<span data-ttu-id="1270c-131">Эта ссылка создается с помощью Get-AzBatchComputeNode и хранения возвращаемого объекта узла вычислений в переменной.</span><span class="sxs-lookup"><span data-stu-id="1270c-131">This object reference is created by using the Get-AzBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

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

### <span data-ttu-id="1270c-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1270c-132">-DefaultProfile</span></span>
<span data-ttu-id="1270c-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1270c-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1270c-134">-Id</span><span class="sxs-lookup"><span data-stu-id="1270c-134">-Id</span></span>
<span data-ttu-id="1270c-135">Определяет ИД узла компьютеров, на котором включено планирование задач.</span><span class="sxs-lookup"><span data-stu-id="1270c-135">Specifies the ID of the compute node where task scheduling is enabled.</span></span>

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

### <span data-ttu-id="1270c-136">-PoolId</span><span class="sxs-lookup"><span data-stu-id="1270c-136">-PoolId</span></span>
<span data-ttu-id="1270c-137">Определяет ИД пула пакетов, который содержит узел вычислений, в котором включено планирование задач.</span><span class="sxs-lookup"><span data-stu-id="1270c-137">Specifies the ID of the batch pool that contains the compute node where task scheduling is enabled.</span></span>

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

### <span data-ttu-id="1270c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1270c-138">CommonParameters</span></span>
<span data-ttu-id="1270c-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1270c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1270c-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1270c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1270c-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1270c-141">INPUTS</span></span>

### <span data-ttu-id="1270c-142">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="1270c-142">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="1270c-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="1270c-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="1270c-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1270c-144">OUTPUTS</span></span>

### <span data-ttu-id="1270c-145">System.Void</span><span class="sxs-lookup"><span data-stu-id="1270c-145">System.Void</span></span>

## <span data-ttu-id="1270c-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1270c-146">NOTES</span></span>

## <span data-ttu-id="1270c-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1270c-147">RELATED LINKS</span></span>

[<span data-ttu-id="1270c-148">Disable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="1270c-148">Disable-AzBatchComputeNodeScheduling</span></span>](./Disable-AzBatchComputeNodeScheduling.md)


