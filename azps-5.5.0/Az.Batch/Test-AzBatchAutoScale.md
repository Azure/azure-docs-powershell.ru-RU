---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: BF0C1A2F-2703-492F-A3A7-053416A5D1EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/test-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Test-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Test-AzBatchAutoScale.md
ms.openlocfilehash: 6732fb89775cea289bf82a5675a482f94b7f95ba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100216100"
---
# <span data-ttu-id="ac899-101">Test-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="ac899-101">Test-AzBatchAutoScale</span></span>

## <span data-ttu-id="ac899-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac899-102">SYNOPSIS</span></span>
<span data-ttu-id="ac899-103">Возвращает результат автоматической формулы масштабирования в пуле.</span><span class="sxs-lookup"><span data-stu-id="ac899-103">Gets the result of an automatic scaling formula on a pool.</span></span>

## <span data-ttu-id="ac899-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ac899-104">SYNTAX</span></span>

```
Test-AzBatchAutoScale [-Id] <String> [-AutoScaleFormula] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac899-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac899-105">DESCRIPTION</span></span>
<span data-ttu-id="ac899-106">Для **этого возвращается** результат автоматической формулы масштабирования для указанного пула.</span><span class="sxs-lookup"><span data-stu-id="ac899-106">The **Test-AzBatchAutoScale** cmdlet gets the result of an automatic scaling formula on the specified pool.</span></span>

## <span data-ttu-id="ac899-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ac899-107">EXAMPLES</span></span>

### <span data-ttu-id="ac899-108">Пример 1. Оценка формулы с авто шкалой в пуле</span><span class="sxs-lookup"><span data-stu-id="ac899-108">Example 1: Evaluate an autoscale formula on a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> $Evaluation = Test-AzBatchAutoScale -Id "ContosoPool" -AutoScaleFormula $Formula -BatchContext $Context
PS C:\> $Evaluation.AutoScaleRun.Results
$TargetDedicated=5;$NodeDeallocationOption=requeue;totalNodes=5
```

<span data-ttu-id="ac899-109">Первая команда сохраняет формулу в переменной $Formula для использования в примере.</span><span class="sxs-lookup"><span data-stu-id="ac899-109">The first command stores a formula in the $Formula variable for use in the example.</span></span>
<span data-ttu-id="ac899-110">Вторая команда оценивает формулу автомасштабы в пуле с ИД ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="ac899-110">The second command evaluates the autoscale formula on the pool that has the ID ContosoPool.</span></span>
<span data-ttu-id="ac899-111">Конечная команда отображает результаты **с** использованием стандартного синтаксиса точки.</span><span class="sxs-lookup"><span data-stu-id="ac899-111">The final command displays the **Results** by using standard dot syntax.</span></span>

## <span data-ttu-id="ac899-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac899-112">PARAMETERS</span></span>

### <span data-ttu-id="ac899-113">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="ac899-113">-AutoScaleFormula</span></span>
<span data-ttu-id="ac899-114">Определяет формулу для нужного количества узлов компьютеров в пуле.</span><span class="sxs-lookup"><span data-stu-id="ac899-114">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac899-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ac899-115">-BatchContext</span></span>
<span data-ttu-id="ac899-116">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="ac899-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ac899-117">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой batchy будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ac899-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ac899-118">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="ac899-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ac899-119">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ac899-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ac899-120">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="ac899-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ac899-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac899-121">-DefaultProfile</span></span>
<span data-ttu-id="ac899-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ac899-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac899-123">-Id</span><span class="sxs-lookup"><span data-stu-id="ac899-123">-Id</span></span>
<span data-ttu-id="ac899-124">Определяет ИД объекта пула, для которого нужно проверить автоматическое масштабирование.</span><span class="sxs-lookup"><span data-stu-id="ac899-124">Specifies the object ID of the pool for which to test automatic scaling.</span></span>

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

### <span data-ttu-id="ac899-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac899-125">CommonParameters</span></span>
<span data-ttu-id="ac899-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac899-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac899-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ac899-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac899-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ac899-128">INPUTS</span></span>

### <span data-ttu-id="ac899-129">System.String</span><span class="sxs-lookup"><span data-stu-id="ac899-129">System.String</span></span>

### <span data-ttu-id="ac899-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ac899-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="ac899-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ac899-131">OUTPUTS</span></span>

### <span data-ttu-id="ac899-132">Microsoft.Azure.Commands.Batch. Models.PSAutoScaleRun</span><span class="sxs-lookup"><span data-stu-id="ac899-132">Microsoft.Azure.Commands.Batch.Models.PSAutoScaleRun</span></span>

## <span data-ttu-id="ac899-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ac899-133">NOTES</span></span>

## <span data-ttu-id="ac899-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ac899-134">RELATED LINKS</span></span>

[<span data-ttu-id="ac899-135">Disable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="ac899-135">Disable-AzBatchAutoScale</span></span>](./Disable-AzBatchAutoScale.md)

[<span data-ttu-id="ac899-136">Enable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="ac899-136">Enable-AzBatchAutoScale</span></span>](./Enable-AzBatchAutoScale.md)

[<span data-ttu-id="ac899-137">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="ac899-137">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="ac899-138">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="ac899-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
