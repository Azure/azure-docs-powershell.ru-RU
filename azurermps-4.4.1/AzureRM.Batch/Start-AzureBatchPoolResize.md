---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 82DC8DC4-D8EC-4847-A54C-B779256FD590
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchPoolResize.md
ms.openlocfilehash: 558f8c062e60f6e9f7c18c05be8f1ccb2eafa9fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566304"
---
# <span data-ttu-id="645d9-101">Start-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="645d9-101">Start-AzureBatchPoolResize</span></span>

## <span data-ttu-id="645d9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="645d9-102">SYNOPSIS</span></span>
<span data-ttu-id="645d9-103">Начало изменения размера пула.</span><span class="sxs-lookup"><span data-stu-id="645d9-103">Starts to resize a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="645d9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="645d9-104">SYNTAX</span></span>

```
Start-AzureBatchPoolResize [-Id] <String> -TargetDedicated <Int32> [-ResizeTimeout <TimeSpan>]
 [-ComputeNodeDeallocationOption <ComputeNodeDeallocationOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="645d9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="645d9-105">DESCRIPTION</span></span>
<span data-ttu-id="645d9-106">Командлет **Start-AzureBatchPoolResize** запускает операцию изменения размера пакета Azure в пуле.</span><span class="sxs-lookup"><span data-stu-id="645d9-106">The **Start-AzureBatchPoolResize** cmdlet starts an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="645d9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="645d9-107">EXAMPLES</span></span>

### <span data-ttu-id="645d9-108">Пример 1: изменение размера пула на 12 узлов</span><span class="sxs-lookup"><span data-stu-id="645d9-108">Example 1: Resize a pool to 12 nodes</span></span>
```
PS C:\>Start-AzureBatchPoolResize -Id "ContosoPool06" -TargetDedicated 12 -BatchContext $Context
```

<span data-ttu-id="645d9-109">Эта команда запускает операцию изменения размера в пуле с ИД ContosoPool06.</span><span class="sxs-lookup"><span data-stu-id="645d9-109">This command starts a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="645d9-110">Цель для операции составляет 12 выделенных вычислительных узлов.</span><span class="sxs-lookup"><span data-stu-id="645d9-110">The target for the operation is 12 dedicated compute nodes.</span></span>
<span data-ttu-id="645d9-111">Используйте командлет Get-AzureRmBatchAccountKeys для присвоения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="645d9-111">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="645d9-112">Пример 2: изменение размера пула с помощью параметра "изъятие"</span><span class="sxs-lookup"><span data-stu-id="645d9-112">Example 2: Resize a pool using a deallocation option</span></span>
```
PS C:\>Get-AzureBatchPool -Id "ContosoPool06" -BatchContext $Context | Start-AzureBatchPoolResize -TargetDedicated 5 -ResizeTimeout ([TimeSpan]::FromHours(1)) -ComputeNodeDeallocationOption ([Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]::Terminate) -BatchContext $Context
```

<span data-ttu-id="645d9-113">Этот командлет изменяет размер пула до пяти выделенных вычислительных узлов.</span><span class="sxs-lookup"><span data-stu-id="645d9-113">This cmdlet resizes a pool to five dedicated compute nodes.</span></span>
<span data-ttu-id="645d9-114">Команда получает пул с ИД ContosoPool06 с помощью командлета Get-AzureBatchPool.</span><span class="sxs-lookup"><span data-stu-id="645d9-114">The command gets the pool that has the ID ContosoPool06 by using the Get-AzureBatchPool cmdlet.</span></span>
<span data-ttu-id="645d9-115">Команда передает этот объект пула в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="645d9-115">The command passes that pool object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="645d9-116">Команда запускает операцию изменения размера в пуле.</span><span class="sxs-lookup"><span data-stu-id="645d9-116">The command starts a resize operation on the pool.</span></span>
<span data-ttu-id="645d9-117">Цель — пять выделенных вычислительных узлов.</span><span class="sxs-lookup"><span data-stu-id="645d9-117">The target is five dedicated compute nodes.</span></span>
<span data-ttu-id="645d9-118">В команде указывается период ожидания в 1 час.</span><span class="sxs-lookup"><span data-stu-id="645d9-118">The command specifies time-out period of one hour.</span></span>
<span data-ttu-id="645d9-119">Команда задает параметр завершения выделения.</span><span class="sxs-lookup"><span data-stu-id="645d9-119">The command specifies a deallocation option of Terminate.</span></span>

## <span data-ttu-id="645d9-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="645d9-120">PARAMETERS</span></span>

### <span data-ttu-id="645d9-121">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="645d9-121">-BatchContext</span></span>
<span data-ttu-id="645d9-122">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="645d9-122">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="645d9-123">Чтобы получить объект **BatchAccountContext** , содержащий клавиши доступа для вашей подписки, используйте командлет Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="645d9-123">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="645d9-124">-ComputeNodeDeallocationOption</span><span class="sxs-lookup"><span data-stu-id="645d9-124">-ComputeNodeDeallocationOption</span></span>
<span data-ttu-id="645d9-125">Задает параметр изъятия для операции изменения размера, которую запускает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="645d9-125">Specifies a deallocation option for the resizing operation that this cmdlet starts.</span></span>

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

### <span data-ttu-id="645d9-126">-ID</span><span class="sxs-lookup"><span data-stu-id="645d9-126">-Id</span></span>
<span data-ttu-id="645d9-127">Указывает идентификатор пула, размер которого изменяется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="645d9-127">Specifies the ID of the pool that this cmdlet resizes.</span></span>

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

### <span data-ttu-id="645d9-128">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="645d9-128">-ResizeTimeout</span></span>
<span data-ttu-id="645d9-129">Задает время ожидания для операции изменения размера.</span><span class="sxs-lookup"><span data-stu-id="645d9-129">Specifies a time-out period for the resizing operation.</span></span>
<span data-ttu-id="645d9-130">Если пул не достиг целевого размера по этому времени, операция изменения размера будет остановлена.</span><span class="sxs-lookup"><span data-stu-id="645d9-130">If the pool does not reach the target size by this time, the resize operation stops.</span></span>

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

### <span data-ttu-id="645d9-131">-TargetDedicated</span><span class="sxs-lookup"><span data-stu-id="645d9-131">-TargetDedicated</span></span>
<span data-ttu-id="645d9-132">Задает целевое количество выделенных вычислительных узлов.</span><span class="sxs-lookup"><span data-stu-id="645d9-132">Specifies the target number of dedicated compute nodes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="645d9-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="645d9-133">-DefaultProfile</span></span>
<span data-ttu-id="645d9-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="645d9-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="645d9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="645d9-135">CommonParameters</span></span>
<span data-ttu-id="645d9-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="645d9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="645d9-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="645d9-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="645d9-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="645d9-138">INPUTS</span></span>

### <span data-ttu-id="645d9-139">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="645d9-139">BatchAccountContext</span></span>
<span data-ttu-id="645d9-140">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="645d9-140">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="645d9-141">Подстрок</span><span class="sxs-lookup"><span data-stu-id="645d9-141">String</span></span>
<span data-ttu-id="645d9-142">Параметр ID принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="645d9-142">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="645d9-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="645d9-143">OUTPUTS</span></span>

## <span data-ttu-id="645d9-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="645d9-144">NOTES</span></span>

## <span data-ttu-id="645d9-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="645d9-145">RELATED LINKS</span></span>

[<span data-ttu-id="645d9-146">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="645d9-146">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="645d9-147">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="645d9-147">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="645d9-148">Остановить-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="645d9-148">Stop-AzureBatchPoolResize</span></span>](./Stop-AzureBatchPoolResize.md)

[<span data-ttu-id="645d9-149">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="645d9-149">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


