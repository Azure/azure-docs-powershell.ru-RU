---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 82DC8DC4-D8EC-4847-A54C-B779256FD590
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/start-azbatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchPoolResize.md
ms.openlocfilehash: d8b03aee736456e549a6c88a0aacfeac1d78744c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509549"
---
# <span data-ttu-id="f2058-101">Start-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="f2058-101">Start-AzBatchPoolResize</span></span>

## <span data-ttu-id="f2058-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2058-102">SYNOPSIS</span></span>
<span data-ttu-id="f2058-103">Начинается с того, чтобы перенаблить пул.</span><span class="sxs-lookup"><span data-stu-id="f2058-103">Starts to resize a pool.</span></span>

## <span data-ttu-id="f2058-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f2058-104">SYNTAX</span></span>

```
Start-AzBatchPoolResize [-Id] <String> [-TargetDedicatedComputeNodes <Int32>]
 [-TargetLowPriorityComputeNodes <Int32>] [-ResizeTimeout <TimeSpan>]
 [-ComputeNodeDeallocationOption <ComputeNodeDeallocationOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2058-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2058-105">DESCRIPTION</span></span>
<span data-ttu-id="f2058-106">Для запуска пакета обработки пула начинается операция **"Запуск-AzBatchPoolResize".**</span><span class="sxs-lookup"><span data-stu-id="f2058-106">The **Start-AzBatchPoolResize** cmdlet starts an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="f2058-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f2058-107">EXAMPLES</span></span>

### <span data-ttu-id="f2058-108">Пример 1. Изме-бильярдного пула на 12 узлов</span><span class="sxs-lookup"><span data-stu-id="f2058-108">Example 1: Resize a pool to 12 nodes</span></span>
```
PS C:\>Start-AzBatchPoolResize -Id "ContosoPool06" -TargetDedicatedComputeNodes 12 -BatchContext $Context
```

<span data-ttu-id="f2058-109">Эта команда запускает операцию по переупорядованию пула с ИД ContosoPool06.</span><span class="sxs-lookup"><span data-stu-id="f2058-109">This command starts a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="f2058-110">Целевой аудиторией операции является 12 выделенных узлов компьютеров.</span><span class="sxs-lookup"><span data-stu-id="f2058-110">The target for the operation is 12 dedicated compute nodes.</span></span>
<span data-ttu-id="f2058-111">Используйте Get-AzBatchAccountKey для назначения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="f2058-111">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="f2058-112">Пример 2. Resize a pool using a deallocation option</span><span class="sxs-lookup"><span data-stu-id="f2058-112">Example 2: Resize a pool using a deallocation option</span></span>
```
PS C:\>Get-AzBatchPool -Id "ContosoPool06" -BatchContext $Context | Start-AzBatchPoolResize -TargetDedicatedComputeNodes 5 -ResizeTimeout ([TimeSpan]::FromHours(1)) -ComputeNodeDeallocationOption ([Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]::Terminate) -BatchContext $Context
```

<span data-ttu-id="f2058-113">Этот cmdlet resizes a pool to five dedicated compute nodes.</span><span class="sxs-lookup"><span data-stu-id="f2058-113">This cmdlet resizes a pool to five dedicated compute nodes.</span></span>
<span data-ttu-id="f2058-114">Команда получает пул с ИД ContosoPool06 с помощью Get-AzBatchPool командлета.</span><span class="sxs-lookup"><span data-stu-id="f2058-114">The command gets the pool that has the ID ContosoPool06 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="f2058-115">Эта команда передает этот объект пула текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="f2058-115">The command passes that pool object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f2058-116">Команда начинает операцию по окнованию пула.</span><span class="sxs-lookup"><span data-stu-id="f2058-116">The command starts a resize operation on the pool.</span></span>
<span data-ttu-id="f2058-117">Целевой аудиторией является пять выделенных узлов для компьютеров.</span><span class="sxs-lookup"><span data-stu-id="f2058-117">The target is five dedicated compute nodes.</span></span>
<span data-ttu-id="f2058-118">Команда определяет период времени ожидания в один час.</span><span class="sxs-lookup"><span data-stu-id="f2058-118">The command specifies time-out period of one hour.</span></span>
<span data-ttu-id="f2058-119">Команда определяет способ размещения сделки в варианте "Завершить".</span><span class="sxs-lookup"><span data-stu-id="f2058-119">The command specifies a deallocation option of Terminate.</span></span>

## <span data-ttu-id="f2058-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2058-120">PARAMETERS</span></span>

### <span data-ttu-id="f2058-121">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f2058-121">-BatchContext</span></span>
<span data-ttu-id="f2058-122">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="f2058-122">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f2058-123">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой пакета будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f2058-123">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f2058-124">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="f2058-124">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f2058-125">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f2058-125">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f2058-126">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="f2058-126">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="f2058-127">-ComputeNodeDeallocationOption</span><span class="sxs-lookup"><span data-stu-id="f2058-127">-ComputeNodeDeallocationOption</span></span>
<span data-ttu-id="f2058-128">Определяет способ размещения сделки для операции, которая запускается этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2058-128">Specifies a deallocation option for the resizing operation that this cmdlet starts.</span></span>

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

### <span data-ttu-id="f2058-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2058-129">-DefaultProfile</span></span>
<span data-ttu-id="f2058-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f2058-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2058-131">-Id</span><span class="sxs-lookup"><span data-stu-id="f2058-131">-Id</span></span>
<span data-ttu-id="f2058-132">Определяет код пула, размер который будет меняться этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2058-132">Specifies the ID of the pool that this cmdlet resizes.</span></span>

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

### <span data-ttu-id="f2058-133">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="f2058-133">-ResizeTimeout</span></span>
<span data-ttu-id="f2058-134">Период времени ожидания для операции.</span><span class="sxs-lookup"><span data-stu-id="f2058-134">Specifies a time-out period for the resizing operation.</span></span>
<span data-ttu-id="f2058-135">Если к этому моменту пул не достигнут целевого размера, операция по окнам размера прекращается.</span><span class="sxs-lookup"><span data-stu-id="f2058-135">If the pool does not reach the target size by this time, the resize operation stops.</span></span>

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

### <span data-ttu-id="f2058-136">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="f2058-136">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="f2058-137">Количество целевых выделенных узлов для компьютеров.</span><span class="sxs-lookup"><span data-stu-id="f2058-137">The number of target dedicated compute nodes.</span></span>

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

### <span data-ttu-id="f2058-138">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="f2058-138">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="f2058-139">Количество целевых узлов для вычисления с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="f2058-139">The number of target low-priority compute nodes.</span></span>

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

### <span data-ttu-id="f2058-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2058-140">CommonParameters</span></span>
<span data-ttu-id="f2058-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2058-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2058-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2058-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2058-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f2058-143">INPUTS</span></span>

### <span data-ttu-id="f2058-144">System.String</span><span class="sxs-lookup"><span data-stu-id="f2058-144">System.String</span></span>

### <span data-ttu-id="f2058-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f2058-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="f2058-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f2058-146">OUTPUTS</span></span>

### <span data-ttu-id="f2058-147">System.Void</span><span class="sxs-lookup"><span data-stu-id="f2058-147">System.Void</span></span>

## <span data-ttu-id="f2058-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f2058-148">NOTES</span></span>

## <span data-ttu-id="f2058-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f2058-149">RELATED LINKS</span></span>

[<span data-ttu-id="f2058-150">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="f2058-150">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="f2058-151">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="f2058-151">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="f2058-152">Stop-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="f2058-152">Stop-AzBatchPoolResize</span></span>](./Stop-AzBatchPoolResize.md)

[<span data-ttu-id="f2058-153">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="f2058-153">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
