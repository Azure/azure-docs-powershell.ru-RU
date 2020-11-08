---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 82DC8DC4-D8EC-4847-A54C-B779256FD590
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/start-azbatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchPoolResize.md
ms.openlocfilehash: d8b03aee736456e549a6c88a0aacfeac1d78744c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249223"
---
# <span data-ttu-id="b4940-101">Start-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="b4940-101">Start-AzBatchPoolResize</span></span>

## <span data-ttu-id="b4940-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b4940-102">SYNOPSIS</span></span>
<span data-ttu-id="b4940-103">Начало изменения размера пула.</span><span class="sxs-lookup"><span data-stu-id="b4940-103">Starts to resize a pool.</span></span>

## <span data-ttu-id="b4940-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b4940-104">SYNTAX</span></span>

```
Start-AzBatchPoolResize [-Id] <String> [-TargetDedicatedComputeNodes <Int32>]
 [-TargetLowPriorityComputeNodes <Int32>] [-ResizeTimeout <TimeSpan>]
 [-ComputeNodeDeallocationOption <ComputeNodeDeallocationOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4940-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4940-105">DESCRIPTION</span></span>
<span data-ttu-id="b4940-106">Командлет **Start-AzBatchPoolResize** запускает операцию изменения размера пакета Azure в пуле.</span><span class="sxs-lookup"><span data-stu-id="b4940-106">The **Start-AzBatchPoolResize** cmdlet starts an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="b4940-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b4940-107">EXAMPLES</span></span>

### <span data-ttu-id="b4940-108">Пример 1: изменение размера пула на 12 узлов</span><span class="sxs-lookup"><span data-stu-id="b4940-108">Example 1: Resize a pool to 12 nodes</span></span>
```
PS C:\>Start-AzBatchPoolResize -Id "ContosoPool06" -TargetDedicatedComputeNodes 12 -BatchContext $Context
```

<span data-ttu-id="b4940-109">Эта команда запускает операцию изменения размера в пуле с ИД ContosoPool06.</span><span class="sxs-lookup"><span data-stu-id="b4940-109">This command starts a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="b4940-110">Цель для операции составляет 12 выделенных вычислительных узлов.</span><span class="sxs-lookup"><span data-stu-id="b4940-110">The target for the operation is 12 dedicated compute nodes.</span></span>
<span data-ttu-id="b4940-111">Используйте командлет Get-AzBatchAccountKey для присвоения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="b4940-111">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="b4940-112">Пример 2: изменение размера пула с помощью параметра "изъятие"</span><span class="sxs-lookup"><span data-stu-id="b4940-112">Example 2: Resize a pool using a deallocation option</span></span>
```
PS C:\>Get-AzBatchPool -Id "ContosoPool06" -BatchContext $Context | Start-AzBatchPoolResize -TargetDedicatedComputeNodes 5 -ResizeTimeout ([TimeSpan]::FromHours(1)) -ComputeNodeDeallocationOption ([Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]::Terminate) -BatchContext $Context
```

<span data-ttu-id="b4940-113">Этот командлет изменяет размер пула до пяти выделенных вычислительных узлов.</span><span class="sxs-lookup"><span data-stu-id="b4940-113">This cmdlet resizes a pool to five dedicated compute nodes.</span></span>
<span data-ttu-id="b4940-114">Команда получает пул с ИД ContosoPool06 с помощью командлета Get-AzBatchPool.</span><span class="sxs-lookup"><span data-stu-id="b4940-114">The command gets the pool that has the ID ContosoPool06 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="b4940-115">Команда передает этот объект пула в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="b4940-115">The command passes that pool object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b4940-116">Команда запускает операцию изменения размера в пуле.</span><span class="sxs-lookup"><span data-stu-id="b4940-116">The command starts a resize operation on the pool.</span></span>
<span data-ttu-id="b4940-117">Цель — пять выделенных вычислительных узлов.</span><span class="sxs-lookup"><span data-stu-id="b4940-117">The target is five dedicated compute nodes.</span></span>
<span data-ttu-id="b4940-118">В команде указывается период ожидания в 1 час.</span><span class="sxs-lookup"><span data-stu-id="b4940-118">The command specifies time-out period of one hour.</span></span>
<span data-ttu-id="b4940-119">Команда задает параметр завершения выделения.</span><span class="sxs-lookup"><span data-stu-id="b4940-119">The command specifies a deallocation option of Terminate.</span></span>

## <span data-ttu-id="b4940-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b4940-120">PARAMETERS</span></span>

### <span data-ttu-id="b4940-121">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b4940-121">-BatchContext</span></span>
<span data-ttu-id="b4940-122">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="b4940-122">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b4940-123">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="b4940-123">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b4940-124">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKey, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="b4940-124">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b4940-125">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="b4940-125">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b4940-126">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="b4940-126">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="b4940-127">-ComputeNodeDeallocationOption</span><span class="sxs-lookup"><span data-stu-id="b4940-127">-ComputeNodeDeallocationOption</span></span>
<span data-ttu-id="b4940-128">Задает параметр изъятия для операции изменения размера, которую запускает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b4940-128">Specifies a deallocation option for the resizing operation that this cmdlet starts.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4940-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4940-129">-DefaultProfile</span></span>
<span data-ttu-id="b4940-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b4940-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4940-131">-ID</span><span class="sxs-lookup"><span data-stu-id="b4940-131">-Id</span></span>
<span data-ttu-id="b4940-132">Указывает идентификатор пула, размер которого изменяется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="b4940-132">Specifies the ID of the pool that this cmdlet resizes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4940-133">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="b4940-133">-ResizeTimeout</span></span>
<span data-ttu-id="b4940-134">Задает время ожидания для операции изменения размера.</span><span class="sxs-lookup"><span data-stu-id="b4940-134">Specifies a time-out period for the resizing operation.</span></span>
<span data-ttu-id="b4940-135">Если пул не достиг целевого размера по этому времени, операция изменения размера будет остановлена.</span><span class="sxs-lookup"><span data-stu-id="b4940-135">If the pool does not reach the target size by this time, the resize operation stops.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4940-136">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="b4940-136">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="b4940-137">Количество целевых выделенных вычислительных узлов.</span><span class="sxs-lookup"><span data-stu-id="b4940-137">The number of target dedicated compute nodes.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: TargetDedicated

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4940-138">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="b4940-138">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="b4940-139">Количество целевых вычислительных узлов с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="b4940-139">The number of target low-priority compute nodes.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4940-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4940-140">CommonParameters</span></span>
<span data-ttu-id="b4940-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b4940-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4940-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4940-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4940-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b4940-143">INPUTS</span></span>

### <span data-ttu-id="b4940-144">System. String</span><span class="sxs-lookup"><span data-stu-id="b4940-144">System.String</span></span>

### <span data-ttu-id="b4940-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b4940-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="b4940-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4940-146">OUTPUTS</span></span>

### <span data-ttu-id="b4940-147">System. void</span><span class="sxs-lookup"><span data-stu-id="b4940-147">System.Void</span></span>

## <span data-ttu-id="b4940-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="b4940-148">NOTES</span></span>

## <span data-ttu-id="b4940-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b4940-149">RELATED LINKS</span></span>

[<span data-ttu-id="b4940-150">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="b4940-150">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="b4940-151">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="b4940-151">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="b4940-152">Остановить-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="b4940-152">Stop-AzBatchPoolResize</span></span>](./Stop-AzBatchPoolResize.md)

[<span data-ttu-id="b4940-153">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="b4940-153">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
