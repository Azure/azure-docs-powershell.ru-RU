---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3107D061-7F25-45D0-8029-C99120A156DA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchAutoScale.md
ms.openlocfilehash: 73e7e9e0e4020f284b26e720e0f34ec7f11fd04f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98411076"
---
# <span data-ttu-id="95c08-101">Enable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="95c08-101">Enable-AzBatchAutoScale</span></span>

## <span data-ttu-id="95c08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95c08-102">SYNOPSIS</span></span>
<span data-ttu-id="95c08-103">Включает автоматическое масштабирование пула.</span><span class="sxs-lookup"><span data-stu-id="95c08-103">Enables automatic scaling of a pool.</span></span>

## <span data-ttu-id="95c08-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="95c08-104">SYNTAX</span></span>

```
Enable-AzBatchAutoScale [-Id] <String> [[-AutoScaleFormula] <String>]
 [[-AutoScaleEvaluationInterval] <TimeSpan>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95c08-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="95c08-105">DESCRIPTION</span></span>
<span data-ttu-id="95c08-106">Для автоматического масштабирования указанного пула можно использовать **cmdlet Enable-AzBatchAutoScale.**</span><span class="sxs-lookup"><span data-stu-id="95c08-106">The **Enable-AzBatchAutoScale** cmdlet enables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="95c08-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="95c08-107">EXAMPLES</span></span>

### <span data-ttu-id="95c08-108">Пример 1. Включив автоматическое масштабирование для пула</span><span class="sxs-lookup"><span data-stu-id="95c08-108">Example 1: Enable automatic scaling for a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> Enable-AzBatchAutoScale -Id "MyPool" -AutoScaleFormula $Formula -BatchContext $Context
```

<span data-ttu-id="95c08-109">Первая команда определяет формулу, а затем сохраняет ее в $Formula переменной.</span><span class="sxs-lookup"><span data-stu-id="95c08-109">The first command defines a formula, and then saves it to the $Formula variable.</span></span>
<span data-ttu-id="95c08-110">Вторая команда включает автоматическое масштабирование пула MyPool с использованием формулы в $Formula.</span><span class="sxs-lookup"><span data-stu-id="95c08-110">The second command enables automatic scaling on the pool named MyPool using the formula in $Formula.</span></span>

## <span data-ttu-id="95c08-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95c08-111">PARAMETERS</span></span>

### <span data-ttu-id="95c08-112">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="95c08-112">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="95c08-113">Определяет время (в минутах), которое будет задано до того, как размер пула будет автоматически скорректирован в соответствии с формулой автомасштаби.</span><span class="sxs-lookup"><span data-stu-id="95c08-113">Specifies the amount of time (in minutes) that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="95c08-114">Значение по умолчанию — 15 минут, минимальное — 5 минут.</span><span class="sxs-lookup"><span data-stu-id="95c08-114">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="95c08-115">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="95c08-115">-AutoScaleFormula</span></span>
<span data-ttu-id="95c08-116">Определяет формулу для нужного количества узлов компьютеров в пуле.</span><span class="sxs-lookup"><span data-stu-id="95c08-116">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

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

### <span data-ttu-id="95c08-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="95c08-117">-BatchContext</span></span>
<span data-ttu-id="95c08-118">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="95c08-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="95c08-119">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой пакета будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="95c08-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="95c08-120">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="95c08-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="95c08-121">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="95c08-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="95c08-122">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="95c08-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="95c08-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95c08-123">-DefaultProfile</span></span>
<span data-ttu-id="95c08-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="95c08-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95c08-125">-Id</span><span class="sxs-lookup"><span data-stu-id="95c08-125">-Id</span></span>
<span data-ttu-id="95c08-126">Определяет ИД объекта пула, для которого нужно включить автоматическое масштабирование.</span><span class="sxs-lookup"><span data-stu-id="95c08-126">Specifies the object ID of the pool for which to enable automatic scaling.</span></span>

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

### <span data-ttu-id="95c08-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95c08-127">CommonParameters</span></span>
<span data-ttu-id="95c08-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95c08-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95c08-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="95c08-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95c08-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="95c08-130">INPUTS</span></span>

### <span data-ttu-id="95c08-131">System.String</span><span class="sxs-lookup"><span data-stu-id="95c08-131">System.String</span></span>

### <span data-ttu-id="95c08-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="95c08-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="95c08-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="95c08-133">OUTPUTS</span></span>

### <span data-ttu-id="95c08-134">System.Void</span><span class="sxs-lookup"><span data-stu-id="95c08-134">System.Void</span></span>

## <span data-ttu-id="95c08-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="95c08-135">NOTES</span></span>

## <span data-ttu-id="95c08-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="95c08-136">RELATED LINKS</span></span>

[<span data-ttu-id="95c08-137">Disable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="95c08-137">Disable-AzBatchAutoScale</span></span>](./Disable-AzBatchAutoScale.md)

[<span data-ttu-id="95c08-138">Test-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="95c08-138">Test-AzBatchAutoScale</span></span>](./Test-AzBatchAutoScale.md)

[<span data-ttu-id="95c08-139">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="95c08-139">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
