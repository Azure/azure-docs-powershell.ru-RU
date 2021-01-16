---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: BF0C1A2F-2703-492F-A3A7-053416A5D1EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/test-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Test-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Test-AzBatchAutoScale.md
ms.openlocfilehash: 6732fb89775cea289bf82a5675a482f94b7f95ba
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409828"
---
# <span data-ttu-id="c996f-101">Test-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="c996f-101">Test-AzBatchAutoScale</span></span>

## <span data-ttu-id="c996f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c996f-102">SYNOPSIS</span></span>
<span data-ttu-id="c996f-103">Возвращает результат автоматической формулы масштабирования в пуле.</span><span class="sxs-lookup"><span data-stu-id="c996f-103">Gets the result of an automatic scaling formula on a pool.</span></span>

## <span data-ttu-id="c996f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c996f-104">SYNTAX</span></span>

```
Test-AzBatchAutoScale [-Id] <String> [-AutoScaleFormula] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c996f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c996f-105">DESCRIPTION</span></span>
<span data-ttu-id="c996f-106">Для **этого возвращается** результат автоматической формулы масштабирования для указанного пула.</span><span class="sxs-lookup"><span data-stu-id="c996f-106">The **Test-AzBatchAutoScale** cmdlet gets the result of an automatic scaling formula on the specified pool.</span></span>

## <span data-ttu-id="c996f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c996f-107">EXAMPLES</span></span>

### <span data-ttu-id="c996f-108">Пример 1. Оценка формулы с авто шкалой в пуле</span><span class="sxs-lookup"><span data-stu-id="c996f-108">Example 1: Evaluate an autoscale formula on a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> $Evaluation = Test-AzBatchAutoScale -Id "ContosoPool" -AutoScaleFormula $Formula -BatchContext $Context
PS C:\> $Evaluation.AutoScaleRun.Results
$TargetDedicated=5;$NodeDeallocationOption=requeue;totalNodes=5
```

<span data-ttu-id="c996f-109">Первая команда хранит формулу в переменной $Formula для использования в примере.</span><span class="sxs-lookup"><span data-stu-id="c996f-109">The first command stores a formula in the $Formula variable for use in the example.</span></span>
<span data-ttu-id="c996f-110">Вторая команда оценивает формулу автомасштабы в пуле с ИД ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="c996f-110">The second command evaluates the autoscale formula on the pool that has the ID ContosoPool.</span></span>
<span data-ttu-id="c996f-111">Конечная команда отображает результаты **с** использованием стандартного синтаксиса точки.</span><span class="sxs-lookup"><span data-stu-id="c996f-111">The final command displays the **Results** by using standard dot syntax.</span></span>

## <span data-ttu-id="c996f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c996f-112">PARAMETERS</span></span>

### <span data-ttu-id="c996f-113">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="c996f-113">-AutoScaleFormula</span></span>
<span data-ttu-id="c996f-114">Определяет формулу для нужного количества узлов компьютеров в пуле.</span><span class="sxs-lookup"><span data-stu-id="c996f-114">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

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

### <span data-ttu-id="c996f-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c996f-115">-BatchContext</span></span>
<span data-ttu-id="c996f-116">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="c996f-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c996f-117">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой пакета будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c996f-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c996f-118">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="c996f-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c996f-119">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c996f-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c996f-120">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="c996f-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c996f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c996f-121">-DefaultProfile</span></span>
<span data-ttu-id="c996f-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c996f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c996f-123">-Id</span><span class="sxs-lookup"><span data-stu-id="c996f-123">-Id</span></span>
<span data-ttu-id="c996f-124">Определяет ИД объекта пула, для которого нужно проверить автоматическое масштабирование.</span><span class="sxs-lookup"><span data-stu-id="c996f-124">Specifies the object ID of the pool for which to test automatic scaling.</span></span>

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

### <span data-ttu-id="c996f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c996f-125">CommonParameters</span></span>
<span data-ttu-id="c996f-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c996f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c996f-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c996f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c996f-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c996f-128">INPUTS</span></span>

### <span data-ttu-id="c996f-129">System.String</span><span class="sxs-lookup"><span data-stu-id="c996f-129">System.String</span></span>

### <span data-ttu-id="c996f-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c996f-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="c996f-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c996f-131">OUTPUTS</span></span>

### <span data-ttu-id="c996f-132">Microsoft.Azure.Commands.Batch. Models.PSAutoScaleRun</span><span class="sxs-lookup"><span data-stu-id="c996f-132">Microsoft.Azure.Commands.Batch.Models.PSAutoScaleRun</span></span>

## <span data-ttu-id="c996f-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c996f-133">NOTES</span></span>

## <span data-ttu-id="c996f-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c996f-134">RELATED LINKS</span></span>

[<span data-ttu-id="c996f-135">Disable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="c996f-135">Disable-AzBatchAutoScale</span></span>](./Disable-AzBatchAutoScale.md)

[<span data-ttu-id="c996f-136">Enable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="c996f-136">Enable-AzBatchAutoScale</span></span>](./Enable-AzBatchAutoScale.md)

[<span data-ttu-id="c996f-137">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="c996f-137">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="c996f-138">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="c996f-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
