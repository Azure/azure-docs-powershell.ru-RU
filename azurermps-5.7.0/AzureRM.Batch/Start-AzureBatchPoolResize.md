---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 82DC8DC4-D8EC-4847-A54C-B779256FD590
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/start-azurebatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchPoolResize.md
ms.openlocfilehash: b460eb4377f06cfa7348f06cdd60f2013e5b5e3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559304"
---
# <span data-ttu-id="14045-101">Start-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="14045-101">Start-AzureBatchPoolResize</span></span>

## <span data-ttu-id="14045-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="14045-102">SYNOPSIS</span></span>
<span data-ttu-id="14045-103">Начало изменения размера пула.</span><span class="sxs-lookup"><span data-stu-id="14045-103">Starts to resize a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14045-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="14045-104">SYNTAX</span></span>

```
Start-AzureBatchPoolResize [-Id] <String> [-TargetDedicatedComputeNodes <Int32>]
 [-TargetLowPriorityComputeNodes <Int32>] [-ResizeTimeout <TimeSpan>]
 [-ComputeNodeDeallocationOption <ComputeNodeDeallocationOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14045-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="14045-105">DESCRIPTION</span></span>
<span data-ttu-id="14045-106">Командлет **Start-AzureBatchPoolResize** запускает операцию изменения размера пакета Azure в пуле.</span><span class="sxs-lookup"><span data-stu-id="14045-106">The **Start-AzureBatchPoolResize** cmdlet starts an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="14045-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="14045-107">EXAMPLES</span></span>

### <span data-ttu-id="14045-108">Пример 1: изменение размера пула на 12 узлов</span><span class="sxs-lookup"><span data-stu-id="14045-108">Example 1: Resize a pool to 12 nodes</span></span>
```
PS C:\>Start-AzureBatchPoolResize -Id "ContosoPool06" -TargetDedicatedComputeNodes 12 -BatchContext $Context
```

<span data-ttu-id="14045-109">Эта команда запускает операцию изменения размера в пуле с ИД ContosoPool06.</span><span class="sxs-lookup"><span data-stu-id="14045-109">This command starts a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="14045-110">Цель для операции составляет 12 выделенных вычислительных узлов.</span><span class="sxs-lookup"><span data-stu-id="14045-110">The target for the operation is 12 dedicated compute nodes.</span></span>
<span data-ttu-id="14045-111">Используйте командлет Get-AzureRmBatchAccountKeys для присвоения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="14045-111">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="14045-112">Пример 2: изменение размера пула с помощью параметра "изъятие"</span><span class="sxs-lookup"><span data-stu-id="14045-112">Example 2: Resize a pool using a deallocation option</span></span>
```
PS C:\>Get-AzureBatchPool -Id "ContosoPool06" -BatchContext $Context | Start-AzureBatchPoolResize -TargetDedicatedComputeNodes 5 -ResizeTimeout ([TimeSpan]::FromHours(1)) -ComputeNodeDeallocationOption ([Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]::Terminate) -BatchContext $Context
```

<span data-ttu-id="14045-113">Этот командлет изменяет размер пула до пяти выделенных вычислительных узлов.</span><span class="sxs-lookup"><span data-stu-id="14045-113">This cmdlet resizes a pool to five dedicated compute nodes.</span></span>
<span data-ttu-id="14045-114">Команда получает пул с ИД ContosoPool06 с помощью командлета Get-AzureBatchPool.</span><span class="sxs-lookup"><span data-stu-id="14045-114">The command gets the pool that has the ID ContosoPool06 by using the Get-AzureBatchPool cmdlet.</span></span>
<span data-ttu-id="14045-115">Команда передает этот объект пула в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="14045-115">The command passes that pool object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="14045-116">Команда запускает операцию изменения размера в пуле.</span><span class="sxs-lookup"><span data-stu-id="14045-116">The command starts a resize operation on the pool.</span></span>
<span data-ttu-id="14045-117">Цель — пять выделенных вычислительных узлов.</span><span class="sxs-lookup"><span data-stu-id="14045-117">The target is five dedicated compute nodes.</span></span>
<span data-ttu-id="14045-118">В команде указывается период ожидания в 1 час.</span><span class="sxs-lookup"><span data-stu-id="14045-118">The command specifies time-out period of one hour.</span></span>
<span data-ttu-id="14045-119">Команда задает параметр завершения выделения.</span><span class="sxs-lookup"><span data-stu-id="14045-119">The command specifies a deallocation option of Terminate.</span></span>

## <span data-ttu-id="14045-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="14045-120">PARAMETERS</span></span>

### <span data-ttu-id="14045-121">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="14045-121">-BatchContext</span></span>
<span data-ttu-id="14045-122">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="14045-122">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="14045-123">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="14045-123">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="14045-124">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="14045-124">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="14045-125">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="14045-125">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="14045-126">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="14045-126">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="14045-127">-ComputeNodeDeallocationOption</span><span class="sxs-lookup"><span data-stu-id="14045-127">-ComputeNodeDeallocationOption</span></span>
<span data-ttu-id="14045-128">Задает параметр изъятия для операции изменения размера, которую запускает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="14045-128">Specifies a deallocation option for the resizing operation that this cmdlet starts.</span></span>

```yaml
Type: ComputeNodeDeallocationOption
Parameter Sets: (All)
Aliases: 
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14045-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14045-129">-DefaultProfile</span></span>
<span data-ttu-id="14045-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="14045-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14045-131">-ID</span><span class="sxs-lookup"><span data-stu-id="14045-131">-Id</span></span>
<span data-ttu-id="14045-132">Указывает идентификатор пула, размер которого изменяется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="14045-132">Specifies the ID of the pool that this cmdlet resizes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14045-133">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="14045-133">-ResizeTimeout</span></span>
<span data-ttu-id="14045-134">Задает время ожидания для операции изменения размера.</span><span class="sxs-lookup"><span data-stu-id="14045-134">Specifies a time-out period for the resizing operation.</span></span>
<span data-ttu-id="14045-135">Если пул не достиг целевого размера по этому времени, операция изменения размера будет остановлена.</span><span class="sxs-lookup"><span data-stu-id="14045-135">If the pool does not reach the target size by this time, the resize operation stops.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14045-136">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="14045-136">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="14045-137">Количество целевых выделенных вычислительных узлов.</span><span class="sxs-lookup"><span data-stu-id="14045-137">The number of target dedicated compute nodes.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: TargetDedicated

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14045-138">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="14045-138">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="14045-139">Количество целевых вычислительных узлов с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="14045-139">The number of target low-priority compute nodes.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14045-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14045-140">CommonParameters</span></span>
<span data-ttu-id="14045-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="14045-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14045-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14045-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14045-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="14045-143">INPUTS</span></span>

### <span data-ttu-id="14045-144">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="14045-144">BatchAccountContext</span></span>
<span data-ttu-id="14045-145">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="14045-145">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="14045-146">Подстрок</span><span class="sxs-lookup"><span data-stu-id="14045-146">String</span></span>
<span data-ttu-id="14045-147">Параметр ID принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="14045-147">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="14045-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="14045-148">OUTPUTS</span></span>

## <span data-ttu-id="14045-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="14045-149">NOTES</span></span>

## <span data-ttu-id="14045-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="14045-150">RELATED LINKS</span></span>

[<span data-ttu-id="14045-151">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="14045-151">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="14045-152">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="14045-152">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="14045-153">Остановить-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="14045-153">Stop-AzureBatchPoolResize</span></span>](./Stop-AzureBatchPoolResize.md)

[<span data-ttu-id="14045-154">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="14045-154">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


