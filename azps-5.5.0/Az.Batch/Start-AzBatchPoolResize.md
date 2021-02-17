---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 82DC8DC4-D8EC-4847-A54C-B779256FD590
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/start-azbatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchPoolResize.md
ms.openlocfilehash: d8b03aee736456e549a6c88a0aacfeac1d78744c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100216108"
---
# <span data-ttu-id="e5109-101">Start-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="e5109-101">Start-AzBatchPoolResize</span></span>

## <span data-ttu-id="e5109-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5109-102">SYNOPSIS</span></span>
<span data-ttu-id="e5109-103">Начинается с того, чтобы перенаблить пул.</span><span class="sxs-lookup"><span data-stu-id="e5109-103">Starts to resize a pool.</span></span>

## <span data-ttu-id="e5109-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e5109-104">SYNTAX</span></span>

```
Start-AzBatchPoolResize [-Id] <String> [-TargetDedicatedComputeNodes <Int32>]
 [-TargetLowPriorityComputeNodes <Int32>] [-ResizeTimeout <TimeSpan>]
 [-ComputeNodeDeallocationOption <ComputeNodeDeallocationOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5109-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5109-105">DESCRIPTION</span></span>
<span data-ttu-id="e5109-106">Для запуска пакета обработки пула начинается операция **"Запуск-AzBatchPoolResize".**</span><span class="sxs-lookup"><span data-stu-id="e5109-106">The **Start-AzBatchPoolResize** cmdlet starts an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="e5109-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e5109-107">EXAMPLES</span></span>

### <span data-ttu-id="e5109-108">Пример 1. Подгонять пул к 12 узлам</span><span class="sxs-lookup"><span data-stu-id="e5109-108">Example 1: Resize a pool to 12 nodes</span></span>
```
PS C:\>Start-AzBatchPoolResize -Id "ContosoPool06" -TargetDedicatedComputeNodes 12 -BatchContext $Context
```

<span data-ttu-id="e5109-109">Эта команда запускает операцию по переупорядованию пула с ИД ContosoPool06.</span><span class="sxs-lookup"><span data-stu-id="e5109-109">This command starts a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="e5109-110">Целевой аудиторией операции является 12 выделенных вычислительных узлов.</span><span class="sxs-lookup"><span data-stu-id="e5109-110">The target for the operation is 12 dedicated compute nodes.</span></span>
<span data-ttu-id="e5109-111">Используйте Get-AzBatchAccountKey для назначения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="e5109-111">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="e5109-112">Пример 2. Resize a pool using a deallocation option</span><span class="sxs-lookup"><span data-stu-id="e5109-112">Example 2: Resize a pool using a deallocation option</span></span>
```
PS C:\>Get-AzBatchPool -Id "ContosoPool06" -BatchContext $Context | Start-AzBatchPoolResize -TargetDedicatedComputeNodes 5 -ResizeTimeout ([TimeSpan]::FromHours(1)) -ComputeNodeDeallocationOption ([Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]::Terminate) -BatchContext $Context
```

<span data-ttu-id="e5109-113">Этот cmdlet resizes a pool to five dedicated compute nodes.</span><span class="sxs-lookup"><span data-stu-id="e5109-113">This cmdlet resizes a pool to five dedicated compute nodes.</span></span>
<span data-ttu-id="e5109-114">Команда получает пул с ИД ContosoPool06 с помощью Get-AzBatchPool командлета.</span><span class="sxs-lookup"><span data-stu-id="e5109-114">The command gets the pool that has the ID ContosoPool06 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="e5109-115">Эта команда передает этот объект пула текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="e5109-115">The command passes that pool object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e5109-116">Команда начинает операцию по окнованию пула.</span><span class="sxs-lookup"><span data-stu-id="e5109-116">The command starts a resize operation on the pool.</span></span>
<span data-ttu-id="e5109-117">Целевой аудиторией является пять выделенных узлов для компьютеров.</span><span class="sxs-lookup"><span data-stu-id="e5109-117">The target is five dedicated compute nodes.</span></span>
<span data-ttu-id="e5109-118">Команда определяет период времени ожидания на один час.</span><span class="sxs-lookup"><span data-stu-id="e5109-118">The command specifies time-out period of one hour.</span></span>
<span data-ttu-id="e5109-119">Команда определяет способ размещения сделки в варианте "Завершить".</span><span class="sxs-lookup"><span data-stu-id="e5109-119">The command specifies a deallocation option of Terminate.</span></span>

## <span data-ttu-id="e5109-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5109-120">PARAMETERS</span></span>

### <span data-ttu-id="e5109-121">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e5109-121">-BatchContext</span></span>
<span data-ttu-id="e5109-122">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="e5109-122">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e5109-123">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой пакета будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e5109-123">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e5109-124">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="e5109-124">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e5109-125">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e5109-125">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e5109-126">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="e5109-126">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e5109-127">-ComputeNodeDeallocationOption</span><span class="sxs-lookup"><span data-stu-id="e5109-127">-ComputeNodeDeallocationOption</span></span>
<span data-ttu-id="e5109-128">Определяет способ размещения сделки для операции, которая запускается этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5109-128">Specifies a deallocation option for the resizing operation that this cmdlet starts.</span></span>

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

### <span data-ttu-id="e5109-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5109-129">-DefaultProfile</span></span>
<span data-ttu-id="e5109-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e5109-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5109-131">-Id</span><span class="sxs-lookup"><span data-stu-id="e5109-131">-Id</span></span>
<span data-ttu-id="e5109-132">Определяет код пула, размер который будет меняться этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5109-132">Specifies the ID of the pool that this cmdlet resizes.</span></span>

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

### <span data-ttu-id="e5109-133">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="e5109-133">-ResizeTimeout</span></span>
<span data-ttu-id="e5109-134">Период времени ожидания для операции.</span><span class="sxs-lookup"><span data-stu-id="e5109-134">Specifies a time-out period for the resizing operation.</span></span>
<span data-ttu-id="e5109-135">Если к этому моменту пул не достигнут целевого размера, операция по окнам размера прекращается.</span><span class="sxs-lookup"><span data-stu-id="e5109-135">If the pool does not reach the target size by this time, the resize operation stops.</span></span>

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

### <span data-ttu-id="e5109-136">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="e5109-136">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="e5109-137">Количество целевых выделенных узлов для компьютеров.</span><span class="sxs-lookup"><span data-stu-id="e5109-137">The number of target dedicated compute nodes.</span></span>

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

### <span data-ttu-id="e5109-138">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="e5109-138">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="e5109-139">Количество целевых узлов для вычисления с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="e5109-139">The number of target low-priority compute nodes.</span></span>

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

### <span data-ttu-id="e5109-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5109-140">CommonParameters</span></span>
<span data-ttu-id="e5109-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5109-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5109-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e5109-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5109-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e5109-143">INPUTS</span></span>

### <span data-ttu-id="e5109-144">System.String</span><span class="sxs-lookup"><span data-stu-id="e5109-144">System.String</span></span>

### <span data-ttu-id="e5109-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e5109-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e5109-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e5109-146">OUTPUTS</span></span>

### <span data-ttu-id="e5109-147">System.Void</span><span class="sxs-lookup"><span data-stu-id="e5109-147">System.Void</span></span>

## <span data-ttu-id="e5109-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e5109-148">NOTES</span></span>

## <span data-ttu-id="e5109-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e5109-149">RELATED LINKS</span></span>

[<span data-ttu-id="e5109-150">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="e5109-150">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="e5109-151">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="e5109-151">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="e5109-152">Stop-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="e5109-152">Stop-AzBatchPoolResize</span></span>](./Stop-AzBatchPoolResize.md)

[<span data-ttu-id="e5109-153">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="e5109-153">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
