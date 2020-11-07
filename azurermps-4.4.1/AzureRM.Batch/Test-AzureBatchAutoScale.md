---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: BF0C1A2F-2703-492F-A3A7-053416A5D1EB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Test-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Test-AzureBatchAutoScale.md
ms.openlocfilehash: 2ab8ca197c1d78980e1683f9572f6d3f6d4d55fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732074"
---
# <span data-ttu-id="63677-101">Test-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="63677-101">Test-AzureBatchAutoScale</span></span>

## <span data-ttu-id="63677-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="63677-102">SYNOPSIS</span></span>
<span data-ttu-id="63677-103">Возвращает результат формулы автоматического масштабирования в пуле.</span><span class="sxs-lookup"><span data-stu-id="63677-103">Gets the result of an automatic scaling formula on a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63677-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="63677-104">SYNTAX</span></span>

```
Test-AzureBatchAutoScale [-Id] <String> [-AutoScaleFormula] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63677-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="63677-105">DESCRIPTION</span></span>
<span data-ttu-id="63677-106">Командлет **Test-AzureBatchAutoScale** возвращает результат формулы автоматического масштабирования в указанном пуле.</span><span class="sxs-lookup"><span data-stu-id="63677-106">The **Test-AzureBatchAutoScale** cmdlet gets the result of an automatic scaling formula on the specified pool.</span></span>

## <span data-ttu-id="63677-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="63677-107">EXAMPLES</span></span>

### <span data-ttu-id="63677-108">Пример 1: вычисление формулы автомасштабирования для пула</span><span class="sxs-lookup"><span data-stu-id="63677-108">Example 1: Evaluate an autoscale formula on a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> $Evaluation = Test-AzureBatchAutoScale -Id "ContosoPool" -AutoScaleFormula $Formula -BatchContext $Context
PS C:\> $Evaluation.AutoScaleRun.Results
$TargetDedicated=5;$NodeDeallocationOption=requeue;totalNodes=5
```

<span data-ttu-id="63677-109">Первая команда сохраняет формулу в $Formula переменной для использования в примере.</span><span class="sxs-lookup"><span data-stu-id="63677-109">The first command stores a formula in the $Formula variable for use in the example.</span></span>

<span data-ttu-id="63677-110">Вторая команда вычисляет формулу автомасштабирования в пуле с ИДЕНТИФИКАТОРом ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="63677-110">The second command evaluates the autoscale formula on the pool that has the ID ContosoPool.</span></span>

<span data-ttu-id="63677-111">Последняя команда отображает **результаты** с помощью стандартного синтаксиса с точкой.</span><span class="sxs-lookup"><span data-stu-id="63677-111">The final command displays the **Results** by using standard dot syntax.</span></span>

## <span data-ttu-id="63677-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="63677-112">PARAMETERS</span></span>

### <span data-ttu-id="63677-113">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="63677-113">-AutoScaleFormula</span></span>
<span data-ttu-id="63677-114">Задает формулу для требуемого количества вычислительных узлов в пуле.</span><span class="sxs-lookup"><span data-stu-id="63677-114">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

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

### <span data-ttu-id="63677-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="63677-115">-BatchContext</span></span>
<span data-ttu-id="63677-116">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="63677-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="63677-117">Чтобы получить объект **BatchAccountContext** , содержащий клавиши доступа для вашей подписки, используйте командлет Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="63677-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="63677-118">-ID</span><span class="sxs-lookup"><span data-stu-id="63677-118">-Id</span></span>
<span data-ttu-id="63677-119">Указывает идентификатор объекта пула, для которого необходимо протестировать автоматическое масштабирование.</span><span class="sxs-lookup"><span data-stu-id="63677-119">Specifies the object ID of the pool for which to test automatic scaling.</span></span>

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

### <span data-ttu-id="63677-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63677-120">-DefaultProfile</span></span>
<span data-ttu-id="63677-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="63677-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63677-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63677-122">CommonParameters</span></span>
<span data-ttu-id="63677-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="63677-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63677-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63677-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63677-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="63677-125">INPUTS</span></span>

### <span data-ttu-id="63677-126">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="63677-126">BatchAccountContext</span></span>
<span data-ttu-id="63677-127">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="63677-127">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="63677-128">Подстрок</span><span class="sxs-lookup"><span data-stu-id="63677-128">String</span></span>
<span data-ttu-id="63677-129">Параметр ID принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="63677-129">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="63677-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="63677-130">OUTPUTS</span></span>

### <span data-ttu-id="63677-131">PSAutoScaleEvaluation</span><span class="sxs-lookup"><span data-stu-id="63677-131">PSAutoScaleEvaluation</span></span>

## <span data-ttu-id="63677-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="63677-132">NOTES</span></span>

## <span data-ttu-id="63677-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="63677-133">RELATED LINKS</span></span>

[<span data-ttu-id="63677-134">Disable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="63677-134">Disable-AzureBatchAutoScale</span></span>](./Disable-AzureBatchAutoScale.md)

[<span data-ttu-id="63677-135">Enable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="63677-135">Enable-AzureBatchAutoScale</span></span>](./Enable-AzureBatchAutoScale.md)

[<span data-ttu-id="63677-136">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="63677-136">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="63677-137">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="63677-137">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


