---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 36EB9CE6-EAC9-471C-97D6-14E882E0F710
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchComputeNodeScheduling.md
ms.openlocfilehash: 7cf3a056ec4266cccac577920f2f5b9292ce03be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568021"
---
# <span data-ttu-id="82fdc-101">Enable-AzureBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="82fdc-101">Enable-AzureBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="82fdc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="82fdc-102">SYNOPSIS</span></span>
<span data-ttu-id="82fdc-103">Включает планирование задач на заданном вычислительном узле.</span><span class="sxs-lookup"><span data-stu-id="82fdc-103">Enables task scheduling on the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82fdc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="82fdc-104">SYNTAX</span></span>

### <span data-ttu-id="82fdc-105">ID (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="82fdc-105">Id (Default)</span></span>
```
Enable-AzureBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82fdc-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="82fdc-106">InputObject</span></span>
```
Enable-AzureBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82fdc-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="82fdc-107">DESCRIPTION</span></span>
<span data-ttu-id="82fdc-108">Командлет **Enable-AzureBatchComputeNodeScheduling** включает планирование задач на заданном вычислительном узле.</span><span class="sxs-lookup"><span data-stu-id="82fdc-108">The **Enable-AzureBatchComputeNodeScheduling** cmdlet enables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="82fdc-109">Вычислительный узел — это виртуальная машина Azure, выделенная для определенной рабочей нагрузки приложения.</span><span class="sxs-lookup"><span data-stu-id="82fdc-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>

## <span data-ttu-id="82fdc-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="82fdc-110">EXAMPLES</span></span>

### <span data-ttu-id="82fdc-111">Пример 1: включение планирования задач на вычислительном узле</span><span class="sxs-lookup"><span data-stu-id="82fdc-111">Example 1: Enable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Enable-AzureBatchComputeNodeScheduling  -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="82fdc-112">Эти команды включают планирование задач на вычислительном узле TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="82fdc-112">These commands enable task scheduling on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="82fdc-113">Для этого в первой команде примера создается ссылка на объект, содержащая ключи учетной записи для пакетной учетной записи contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="82fdc-113">To do this, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="82fdc-114">Эта ссылка на объект хранится в переменной с именем $context.</span><span class="sxs-lookup"><span data-stu-id="82fdc-114">This object reference is stored in a variable named $context.</span></span>

<span data-ttu-id="82fdc-115">Вторая команда использует эту ссылку на объект и командлет **Enable-AzureBatchComputeNodeScheduling** для подключения к пулу myPool и включения планирования задач в TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="82fdc-115">The second command then uses this object reference and the **Enable-AzureBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and enable task scheduling on tvm-1783593343_34-20151117t222514z.</span></span>

### <span data-ttu-id="82fdc-116">Пример 2: включение планирования задач на вычислительных узлах в пуле</span><span class="sxs-lookup"><span data-stu-id="82fdc-116">Example 2: Enable task scheduling on compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzureBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Enable-AzureBatchComputeNodeScheduling  -BatchContext $Context
```

<span data-ttu-id="82fdc-117">Эти команды включают планирование задач на всех вычислительных узлах, обнаруженных в пуле Pool06.</span><span class="sxs-lookup"><span data-stu-id="82fdc-117">These commands enable task scheduling on all the compute nodes found in the pool Pool06.</span></span>
<span data-ttu-id="82fdc-118">Для выполнения этой задачи в первой команде в примере создается ссылка на объект с ключами учетной записи для пакетной учетной записи contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="82fdc-118">To perform this task, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="82fdc-119">Эта ссылка на объект хранится в переменной с именем $context.</span><span class="sxs-lookup"><span data-stu-id="82fdc-119">This object reference is stored in a variable named $context.</span></span>

<span data-ttu-id="82fdc-120">Во второй команде в примере используется ссылка на объект и **Get-AzureBatchComputeNode** , чтобы вернуть коллекцию всех вычислительных узлов, обнаруженных в Pool06.</span><span class="sxs-lookup"><span data-stu-id="82fdc-120">The second command in the example then uses this object reference and **Get-AzureBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="82fdc-121">Затем эта коллекция передается командлету **Enable-AzureBatchComputeNodeScheduling** , который включает планирование задач на каждом из вычислительных узлов коллекции.</span><span class="sxs-lookup"><span data-stu-id="82fdc-121">That collection is then piped to the **Enable-AzureBatchComputeNodeScheduling** cmdlet, which enables task scheduling on each compute node in the collection.</span></span>

## <span data-ttu-id="82fdc-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="82fdc-122">PARAMETERS</span></span>

### <span data-ttu-id="82fdc-123">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="82fdc-123">-BatchContext</span></span>
<span data-ttu-id="82fdc-124">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="82fdc-124">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="82fdc-125">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="82fdc-125">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="82fdc-126">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="82fdc-126">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="82fdc-127">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="82fdc-127">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="82fdc-128">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="82fdc-128">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="82fdc-129">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="82fdc-129">-ComputeNode</span></span>
<span data-ttu-id="82fdc-130">Указывает ссылку на объект на вычислительный узел, для которого включено планирование задач.</span><span class="sxs-lookup"><span data-stu-id="82fdc-130">Specifies an object reference to the compute node where task scheduling is enabled.</span></span>
<span data-ttu-id="82fdc-131">Эта ссылка на объект создается с помощью командлета Get-AzureBatchComputeNode и сохраняет возвращаемый объект COMPUTE Node в переменной.</span><span class="sxs-lookup"><span data-stu-id="82fdc-131">This object reference is created by using the Get-AzureBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

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

### <span data-ttu-id="82fdc-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82fdc-132">-DefaultProfile</span></span>
<span data-ttu-id="82fdc-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="82fdc-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82fdc-134">-ID</span><span class="sxs-lookup"><span data-stu-id="82fdc-134">-Id</span></span>
<span data-ttu-id="82fdc-135">Указывает идентификатор вычислительного узла, на котором включено планирование задач.</span><span class="sxs-lookup"><span data-stu-id="82fdc-135">Specifies the ID of the compute node where task scheduling is enabled.</span></span>

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

### <span data-ttu-id="82fdc-136">-PoolId</span><span class="sxs-lookup"><span data-stu-id="82fdc-136">-PoolId</span></span>
<span data-ttu-id="82fdc-137">Указывает идентификатор пула пакетов, содержащего вычислительный узел, для которого включено планирование задач.</span><span class="sxs-lookup"><span data-stu-id="82fdc-137">Specifies the ID of the batch pool that contains the compute node where task scheduling is enabled.</span></span>

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

### <span data-ttu-id="82fdc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82fdc-138">CommonParameters</span></span>
<span data-ttu-id="82fdc-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="82fdc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82fdc-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82fdc-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82fdc-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="82fdc-141">INPUTS</span></span>

### <span data-ttu-id="82fdc-142">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="82fdc-142">BatchAccountContext</span></span>
<span data-ttu-id="82fdc-143">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="82fdc-143">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="82fdc-144">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="82fdc-144">PSComputeNode</span></span>
<span data-ttu-id="82fdc-145">Параметр "ComputeNode" принимает значение типа "PSComputeNode" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="82fdc-145">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="82fdc-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="82fdc-146">OUTPUTS</span></span>

## <span data-ttu-id="82fdc-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="82fdc-147">NOTES</span></span>

## <span data-ttu-id="82fdc-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="82fdc-148">RELATED LINKS</span></span>

[<span data-ttu-id="82fdc-149">Disable-AzureBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="82fdc-149">Disable-AzureBatchComputeNodeScheduling</span></span>](./Disable-AzureBatchComputeNodeScheduling.md)


