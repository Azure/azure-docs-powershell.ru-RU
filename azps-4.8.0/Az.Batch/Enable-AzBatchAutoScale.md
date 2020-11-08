---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3107D061-7F25-45D0-8029-C99120A156DA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchAutoScale.md
ms.openlocfilehash: 73e7e9e0e4020f284b26e720e0f34ec7f11fd04f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243709"
---
# <span data-ttu-id="10805-101">Enable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="10805-101">Enable-AzBatchAutoScale</span></span>

## <span data-ttu-id="10805-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="10805-102">SYNOPSIS</span></span>
<span data-ttu-id="10805-103">Включает автоматическое масштабирование пула.</span><span class="sxs-lookup"><span data-stu-id="10805-103">Enables automatic scaling of a pool.</span></span>

## <span data-ttu-id="10805-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="10805-104">SYNTAX</span></span>

```
Enable-AzBatchAutoScale [-Id] <String> [[-AutoScaleFormula] <String>]
 [[-AutoScaleEvaluationInterval] <TimeSpan>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10805-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="10805-105">DESCRIPTION</span></span>
<span data-ttu-id="10805-106">Командлет **Enable-AzBatchAutoScale** включает автоматическое масштабирование указанного пула.</span><span class="sxs-lookup"><span data-stu-id="10805-106">The **Enable-AzBatchAutoScale** cmdlet enables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="10805-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="10805-107">EXAMPLES</span></span>

### <span data-ttu-id="10805-108">Пример 1: Включение автоматического масштабирования для пула</span><span class="sxs-lookup"><span data-stu-id="10805-108">Example 1: Enable automatic scaling for a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> Enable-AzBatchAutoScale -Id "MyPool" -AutoScaleFormula $Formula -BatchContext $Context
```

<span data-ttu-id="10805-109">Первая команда определяет формулу, а затем сохраняет ее в $Formula переменной.</span><span class="sxs-lookup"><span data-stu-id="10805-109">The first command defines a formula, and then saves it to the $Formula variable.</span></span>
<span data-ttu-id="10805-110">Вторая команда включает автоматическое масштабирование в пуле с именем MyPool, используя формулу в $Formula.</span><span class="sxs-lookup"><span data-stu-id="10805-110">The second command enables automatic scaling on the pool named MyPool using the formula in $Formula.</span></span>

## <span data-ttu-id="10805-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="10805-111">PARAMETERS</span></span>

### <span data-ttu-id="10805-112">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="10805-112">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="10805-113">Определяет интервал времени (в минутах), по истечении которого размер пула будет автоматически скорректирован согласно формуле автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="10805-113">Specifies the amount of time (in minutes) that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="10805-114">По умолчанию используется значение 15 минут, а минимальное — 5 минут.</span><span class="sxs-lookup"><span data-stu-id="10805-114">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10805-115">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="10805-115">-AutoScaleFormula</span></span>
<span data-ttu-id="10805-116">Задает формулу для требуемого количества вычислительных узлов в пуле.</span><span class="sxs-lookup"><span data-stu-id="10805-116">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10805-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="10805-117">-BatchContext</span></span>
<span data-ttu-id="10805-118">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="10805-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="10805-119">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="10805-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="10805-120">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKey, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="10805-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="10805-121">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="10805-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="10805-122">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="10805-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="10805-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10805-123">-DefaultProfile</span></span>
<span data-ttu-id="10805-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="10805-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10805-125">-ID</span><span class="sxs-lookup"><span data-stu-id="10805-125">-Id</span></span>
<span data-ttu-id="10805-126">Указывает идентификатор объекта пула, для которого нужно включить автоматическое масштабирование.</span><span class="sxs-lookup"><span data-stu-id="10805-126">Specifies the object ID of the pool for which to enable automatic scaling.</span></span>

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

### <span data-ttu-id="10805-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10805-127">CommonParameters</span></span>
<span data-ttu-id="10805-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="10805-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10805-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="10805-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10805-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="10805-130">INPUTS</span></span>

### <span data-ttu-id="10805-131">System. String</span><span class="sxs-lookup"><span data-stu-id="10805-131">System.String</span></span>

### <span data-ttu-id="10805-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="10805-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="10805-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="10805-133">OUTPUTS</span></span>

### <span data-ttu-id="10805-134">System. void</span><span class="sxs-lookup"><span data-stu-id="10805-134">System.Void</span></span>

## <span data-ttu-id="10805-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="10805-135">NOTES</span></span>

## <span data-ttu-id="10805-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="10805-136">RELATED LINKS</span></span>

[<span data-ttu-id="10805-137">Disable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="10805-137">Disable-AzBatchAutoScale</span></span>](./Disable-AzBatchAutoScale.md)

[<span data-ttu-id="10805-138">Test-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="10805-138">Test-AzBatchAutoScale</span></span>](./Test-AzBatchAutoScale.md)

[<span data-ttu-id="10805-139">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="10805-139">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
