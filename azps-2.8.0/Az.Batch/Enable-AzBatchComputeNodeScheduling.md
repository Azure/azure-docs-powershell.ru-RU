---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 36EB9CE6-EAC9-471C-97D6-14E882E0F710
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 2922e9b1a37f714b1ccfb19aea86556b9988ccca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727708"
---
# <span data-ttu-id="def92-101">Enable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="def92-101">Enable-AzBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="def92-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="def92-102">SYNOPSIS</span></span>
<span data-ttu-id="def92-103">Включает планирование задач на заданном вычислительном узле.</span><span class="sxs-lookup"><span data-stu-id="def92-103">Enables task scheduling on the specified compute node.</span></span>

## <span data-ttu-id="def92-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="def92-104">SYNTAX</span></span>

### <span data-ttu-id="def92-105">ID (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="def92-105">Id (Default)</span></span>
```
Enable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="def92-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="def92-106">InputObject</span></span>
```
Enable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="def92-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="def92-107">DESCRIPTION</span></span>
<span data-ttu-id="def92-108">Командлет **Enable-AzBatchComputeNodeScheduling** включает планирование задач на заданном вычислительном узле.</span><span class="sxs-lookup"><span data-stu-id="def92-108">The **Enable-AzBatchComputeNodeScheduling** cmdlet enables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="def92-109">Вычислительный узел — это виртуальная машина Azure, выделенная для определенной рабочей нагрузки приложения.</span><span class="sxs-lookup"><span data-stu-id="def92-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>

## <span data-ttu-id="def92-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="def92-110">EXAMPLES</span></span>

### <span data-ttu-id="def92-111">Пример 1: включение планирования задач на вычислительном узле</span><span class="sxs-lookup"><span data-stu-id="def92-111">Example 1: Enable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Enable-AzBatchComputeNodeScheduling  -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="def92-112">Эти команды включают планирование задач на вычислительном узле TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="def92-112">These commands enable task scheduling on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="def92-113">Для этого в первой команде примера создается ссылка на объект, содержащая ключи учетной записи для пакетной учетной записи contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="def92-113">To do this, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="def92-114">Эта ссылка на объект хранится в переменной с именем $context.</span><span class="sxs-lookup"><span data-stu-id="def92-114">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="def92-115">Вторая команда использует эту ссылку на объект и командлет **Enable-AzBatchComputeNodeScheduling** для подключения к пулу myPool и включения планирования задач в TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="def92-115">The second command then uses this object reference and the **Enable-AzBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and enable task scheduling on tvm-1783593343_34-20151117t222514z.</span></span>

### <span data-ttu-id="def92-116">Пример 2: включение планирования задач на вычислительных узлах в пуле</span><span class="sxs-lookup"><span data-stu-id="def92-116">Example 2: Enable task scheduling on compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Enable-AzBatchComputeNodeScheduling  -BatchContext $Context
```

<span data-ttu-id="def92-117">Эти команды включают планирование задач на всех вычислительных узлах, обнаруженных в пуле Pool06.</span><span class="sxs-lookup"><span data-stu-id="def92-117">These commands enable task scheduling on all the compute nodes found in the pool Pool06.</span></span>
<span data-ttu-id="def92-118">Для выполнения этой задачи в первой команде в примере создается ссылка на объект с ключами учетной записи для пакетной учетной записи contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="def92-118">To perform this task, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="def92-119">Эта ссылка на объект хранится в переменной с именем $context.</span><span class="sxs-lookup"><span data-stu-id="def92-119">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="def92-120">Во второй команде в примере используется ссылка на объект и **Get-AzBatchComputeNode** , чтобы вернуть коллекцию всех вычислительных узлов, обнаруженных в Pool06.</span><span class="sxs-lookup"><span data-stu-id="def92-120">The second command in the example then uses this object reference and **Get-AzBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="def92-121">Затем эта коллекция передается командлету **Enable-AzBatchComputeNodeScheduling** , который включает планирование задач на каждом из вычислительных узлов коллекции.</span><span class="sxs-lookup"><span data-stu-id="def92-121">That collection is then piped to the **Enable-AzBatchComputeNodeScheduling** cmdlet, which enables task scheduling on each compute node in the collection.</span></span>

## <span data-ttu-id="def92-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="def92-122">PARAMETERS</span></span>

### <span data-ttu-id="def92-123">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="def92-123">-BatchContext</span></span>
<span data-ttu-id="def92-124">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="def92-124">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="def92-125">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="def92-125">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="def92-126">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="def92-126">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="def92-127">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="def92-127">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="def92-128">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="def92-128">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="def92-129">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="def92-129">-ComputeNode</span></span>
<span data-ttu-id="def92-130">Указывает ссылку на объект на вычислительный узел, для которого включено планирование задач.</span><span class="sxs-lookup"><span data-stu-id="def92-130">Specifies an object reference to the compute node where task scheduling is enabled.</span></span>
<span data-ttu-id="def92-131">Эта ссылка на объект создается с помощью командлета Get-AzBatchComputeNode и сохраняет возвращаемый объект COMPUTE Node в переменной.</span><span class="sxs-lookup"><span data-stu-id="def92-131">This object reference is created by using the Get-AzBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

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

### <span data-ttu-id="def92-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="def92-132">-DefaultProfile</span></span>
<span data-ttu-id="def92-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="def92-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="def92-134">-ID</span><span class="sxs-lookup"><span data-stu-id="def92-134">-Id</span></span>
<span data-ttu-id="def92-135">Указывает идентификатор вычислительного узла, на котором включено планирование задач.</span><span class="sxs-lookup"><span data-stu-id="def92-135">Specifies the ID of the compute node where task scheduling is enabled.</span></span>

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

### <span data-ttu-id="def92-136">-PoolId</span><span class="sxs-lookup"><span data-stu-id="def92-136">-PoolId</span></span>
<span data-ttu-id="def92-137">Указывает идентификатор пула пакетов, содержащего вычислительный узел, для которого включено планирование задач.</span><span class="sxs-lookup"><span data-stu-id="def92-137">Specifies the ID of the batch pool that contains the compute node where task scheduling is enabled.</span></span>

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

### <span data-ttu-id="def92-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="def92-138">CommonParameters</span></span>
<span data-ttu-id="def92-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="def92-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="def92-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="def92-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="def92-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="def92-141">INPUTS</span></span>

### <span data-ttu-id="def92-142">Microsoft.Azure.Commands.BatCH. Models. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="def92-142">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="def92-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="def92-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="def92-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="def92-144">OUTPUTS</span></span>

### <span data-ttu-id="def92-145">System. void</span><span class="sxs-lookup"><span data-stu-id="def92-145">System.Void</span></span>

## <span data-ttu-id="def92-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="def92-146">NOTES</span></span>

## <span data-ttu-id="def92-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="def92-147">RELATED LINKS</span></span>

[<span data-ttu-id="def92-148">Disable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="def92-148">Disable-AzBatchComputeNodeScheduling</span></span>](./Disable-AzBatchComputeNodeScheduling.md)


