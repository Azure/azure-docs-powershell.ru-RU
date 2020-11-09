---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: BF0C1A2F-2703-492F-A3A7-053416A5D1EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/test-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Test-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Test-AzBatchAutoScale.md
ms.openlocfilehash: 6732fb89775cea289bf82a5675a482f94b7f95ba
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318674"
---
# <span data-ttu-id="98f34-101">Test-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="98f34-101">Test-AzBatchAutoScale</span></span>

## <span data-ttu-id="98f34-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="98f34-102">SYNOPSIS</span></span>
<span data-ttu-id="98f34-103">Возвращает результат формулы автоматического масштабирования в пуле.</span><span class="sxs-lookup"><span data-stu-id="98f34-103">Gets the result of an automatic scaling formula on a pool.</span></span>

## <span data-ttu-id="98f34-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="98f34-104">SYNTAX</span></span>

```
Test-AzBatchAutoScale [-Id] <String> [-AutoScaleFormula] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98f34-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="98f34-105">DESCRIPTION</span></span>
<span data-ttu-id="98f34-106">Командлет **Test-AzBatchAutoScale** возвращает результат формулы автоматического масштабирования в указанном пуле.</span><span class="sxs-lookup"><span data-stu-id="98f34-106">The **Test-AzBatchAutoScale** cmdlet gets the result of an automatic scaling formula on the specified pool.</span></span>

## <span data-ttu-id="98f34-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="98f34-107">EXAMPLES</span></span>

### <span data-ttu-id="98f34-108">Пример 1: вычисление формулы автомасштабирования для пула</span><span class="sxs-lookup"><span data-stu-id="98f34-108">Example 1: Evaluate an autoscale formula on a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> $Evaluation = Test-AzBatchAutoScale -Id "ContosoPool" -AutoScaleFormula $Formula -BatchContext $Context
PS C:\> $Evaluation.AutoScaleRun.Results
$TargetDedicated=5;$NodeDeallocationOption=requeue;totalNodes=5
```

<span data-ttu-id="98f34-109">Первая команда сохраняет формулу в $Formula переменной для использования в примере.</span><span class="sxs-lookup"><span data-stu-id="98f34-109">The first command stores a formula in the $Formula variable for use in the example.</span></span>
<span data-ttu-id="98f34-110">Вторая команда вычисляет формулу автомасштабирования в пуле с ИДЕНТИФИКАТОРом ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="98f34-110">The second command evaluates the autoscale formula on the pool that has the ID ContosoPool.</span></span>
<span data-ttu-id="98f34-111">Последняя команда отображает **результаты** с помощью стандартного синтаксиса с точкой.</span><span class="sxs-lookup"><span data-stu-id="98f34-111">The final command displays the **Results** by using standard dot syntax.</span></span>

## <span data-ttu-id="98f34-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="98f34-112">PARAMETERS</span></span>

### <span data-ttu-id="98f34-113">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="98f34-113">-AutoScaleFormula</span></span>
<span data-ttu-id="98f34-114">Задает формулу для требуемого количества вычислительных узлов в пуле.</span><span class="sxs-lookup"><span data-stu-id="98f34-114">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

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

### <span data-ttu-id="98f34-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="98f34-115">-BatchContext</span></span>
<span data-ttu-id="98f34-116">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="98f34-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="98f34-117">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="98f34-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="98f34-118">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKey, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="98f34-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="98f34-119">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="98f34-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="98f34-120">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="98f34-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="98f34-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98f34-121">-DefaultProfile</span></span>
<span data-ttu-id="98f34-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="98f34-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98f34-123">-ID</span><span class="sxs-lookup"><span data-stu-id="98f34-123">-Id</span></span>
<span data-ttu-id="98f34-124">Указывает идентификатор объекта пула, для которого необходимо протестировать автоматическое масштабирование.</span><span class="sxs-lookup"><span data-stu-id="98f34-124">Specifies the object ID of the pool for which to test automatic scaling.</span></span>

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

### <span data-ttu-id="98f34-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98f34-125">CommonParameters</span></span>
<span data-ttu-id="98f34-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="98f34-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98f34-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98f34-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98f34-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="98f34-128">INPUTS</span></span>

### <span data-ttu-id="98f34-129">System. String</span><span class="sxs-lookup"><span data-stu-id="98f34-129">System.String</span></span>

### <span data-ttu-id="98f34-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="98f34-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="98f34-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="98f34-131">OUTPUTS</span></span>

### <span data-ttu-id="98f34-132">Microsoft.Azure.Commands.BatCH. Models. PSAutoScaleRun</span><span class="sxs-lookup"><span data-stu-id="98f34-132">Microsoft.Azure.Commands.Batch.Models.PSAutoScaleRun</span></span>

## <span data-ttu-id="98f34-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="98f34-133">NOTES</span></span>

## <span data-ttu-id="98f34-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="98f34-134">RELATED LINKS</span></span>

[<span data-ttu-id="98f34-135">Disable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="98f34-135">Disable-AzBatchAutoScale</span></span>](./Disable-AzBatchAutoScale.md)

[<span data-ttu-id="98f34-136">Enable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="98f34-136">Enable-AzBatchAutoScale</span></span>](./Enable-AzBatchAutoScale.md)

[<span data-ttu-id="98f34-137">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="98f34-137">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="98f34-138">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="98f34-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
