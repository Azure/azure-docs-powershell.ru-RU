---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: BF0C1A2F-2703-492F-A3A7-053416A5D1EB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/test-azurebatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Test-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Test-AzureBatchAutoScale.md
ms.openlocfilehash: 3dc458c5b23e3bd6f8bde39e02152e8c2b76f6f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566838"
---
# <span data-ttu-id="3acef-101">Test-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="3acef-101">Test-AzureBatchAutoScale</span></span>

## <span data-ttu-id="3acef-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3acef-102">SYNOPSIS</span></span>
<span data-ttu-id="3acef-103">Возвращает результат формулы автоматического масштабирования в пуле.</span><span class="sxs-lookup"><span data-stu-id="3acef-103">Gets the result of an automatic scaling formula on a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3acef-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3acef-104">SYNTAX</span></span>

```
Test-AzureBatchAutoScale [-Id] <String> [-AutoScaleFormula] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3acef-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3acef-105">DESCRIPTION</span></span>
<span data-ttu-id="3acef-106">Командлет **Test-AzureBatchAutoScale** возвращает результат формулы автоматического масштабирования в указанном пуле.</span><span class="sxs-lookup"><span data-stu-id="3acef-106">The **Test-AzureBatchAutoScale** cmdlet gets the result of an automatic scaling formula on the specified pool.</span></span>

## <span data-ttu-id="3acef-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3acef-107">EXAMPLES</span></span>

### <span data-ttu-id="3acef-108">Пример 1: вычисление формулы автомасштабирования для пула</span><span class="sxs-lookup"><span data-stu-id="3acef-108">Example 1: Evaluate an autoscale formula on a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> $Evaluation = Test-AzureBatchAutoScale -Id "ContosoPool" -AutoScaleFormula $Formula -BatchContext $Context
PS C:\> $Evaluation.AutoScaleRun.Results
$TargetDedicated=5;$NodeDeallocationOption=requeue;totalNodes=5
```

<span data-ttu-id="3acef-109">Первая команда сохраняет формулу в $Formula переменной для использования в примере.</span><span class="sxs-lookup"><span data-stu-id="3acef-109">The first command stores a formula in the $Formula variable for use in the example.</span></span>
<span data-ttu-id="3acef-110">Вторая команда вычисляет формулу автомасштабирования в пуле с ИДЕНТИФИКАТОРом ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="3acef-110">The second command evaluates the autoscale formula on the pool that has the ID ContosoPool.</span></span>
<span data-ttu-id="3acef-111">Последняя команда отображает **результаты** с помощью стандартного синтаксиса с точкой.</span><span class="sxs-lookup"><span data-stu-id="3acef-111">The final command displays the **Results** by using standard dot syntax.</span></span>

## <span data-ttu-id="3acef-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3acef-112">PARAMETERS</span></span>

### <span data-ttu-id="3acef-113">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="3acef-113">-AutoScaleFormula</span></span>
<span data-ttu-id="3acef-114">Задает формулу для требуемого количества вычислительных узлов в пуле.</span><span class="sxs-lookup"><span data-stu-id="3acef-114">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

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

### <span data-ttu-id="3acef-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="3acef-115">-BatchContext</span></span>
<span data-ttu-id="3acef-116">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="3acef-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="3acef-117">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="3acef-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="3acef-118">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="3acef-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="3acef-119">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="3acef-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="3acef-120">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="3acef-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="3acef-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3acef-121">-DefaultProfile</span></span>
<span data-ttu-id="3acef-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3acef-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3acef-123">-ID</span><span class="sxs-lookup"><span data-stu-id="3acef-123">-Id</span></span>
<span data-ttu-id="3acef-124">Указывает идентификатор объекта пула, для которого необходимо протестировать автоматическое масштабирование.</span><span class="sxs-lookup"><span data-stu-id="3acef-124">Specifies the object ID of the pool for which to test automatic scaling.</span></span>

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

### <span data-ttu-id="3acef-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3acef-125">CommonParameters</span></span>
<span data-ttu-id="3acef-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3acef-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3acef-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3acef-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3acef-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3acef-128">INPUTS</span></span>

### <span data-ttu-id="3acef-129">System. String</span><span class="sxs-lookup"><span data-stu-id="3acef-129">System.String</span></span>

### <span data-ttu-id="3acef-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="3acef-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="3acef-131">Параметры: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3acef-131">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="3acef-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3acef-132">OUTPUTS</span></span>

### <span data-ttu-id="3acef-133">Microsoft.Azure.Commands.BatCH. Models. PSAutoScaleRun</span><span class="sxs-lookup"><span data-stu-id="3acef-133">Microsoft.Azure.Commands.Batch.Models.PSAutoScaleRun</span></span>

## <span data-ttu-id="3acef-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="3acef-134">NOTES</span></span>

## <span data-ttu-id="3acef-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3acef-135">RELATED LINKS</span></span>

[<span data-ttu-id="3acef-136">Disable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="3acef-136">Disable-AzureBatchAutoScale</span></span>](./Disable-AzureBatchAutoScale.md)

[<span data-ttu-id="3acef-137">Enable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="3acef-137">Enable-AzureBatchAutoScale</span></span>](./Enable-AzureBatchAutoScale.md)

[<span data-ttu-id="3acef-138">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="3acef-138">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="3acef-139">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="3acef-139">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


