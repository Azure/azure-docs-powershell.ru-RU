---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 4B373447-3078-4C1F-932E-8337AB170DEB
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchpoolusagemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolUsageMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolUsageMetric.md
ms.openlocfilehash: 1700e20318a502f32386638f94a9c5c86c271d7d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242610"
---
# <span data-ttu-id="98ab1-101">Get-AzBatchPoolUsageMetric</span><span class="sxs-lookup"><span data-stu-id="98ab1-101">Get-AzBatchPoolUsageMetric</span></span>

## <span data-ttu-id="98ab1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="98ab1-102">SYNOPSIS</span></span>
<span data-ttu-id="98ab1-103">Получает метрики использования пула для учетной записи пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="98ab1-103">Gets pool usage metrics for a Batch account.</span></span>

## <span data-ttu-id="98ab1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="98ab1-104">SYNTAX</span></span>

```
Get-AzBatchPoolUsageMetric [-StartTime <DateTime>] [-EndTime <DateTime>] [-Filter <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98ab1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="98ab1-105">DESCRIPTION</span></span>
<span data-ttu-id="98ab1-106">Командлет **Get-AzBatchPoolUsageMetric** получает метрики использования, агрегированные по пулам между отдельными интервалами времени для указанной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="98ab1-106">The **Get-AzBatchPoolUsageMetric** cmdlet gets the usage metrics, aggregated by pool across individual time intervals, for the specified account.</span></span>
<span data-ttu-id="98ab1-107">Вы можете получить статистику для определенного пула и для интервала времени.</span><span class="sxs-lookup"><span data-stu-id="98ab1-107">You can get the statistics for a specific pool and for a time range.</span></span>

## <span data-ttu-id="98ab1-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="98ab1-108">EXAMPLES</span></span>

### <span data-ttu-id="98ab1-109">Пример 1: Получение метрик использования пула для диапазона времени</span><span class="sxs-lookup"><span data-stu-id="98ab1-109">Example 1: Get pool usage metrics for a time range</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> $StartTime = Get-Date -Date "2016-05-16 00:00:00Z"
PS C:\> $EndTime = Get-Date -Date "2016-05-16 01:00:00Z"
PS C:\> Get-AzBatchPoolUsageMetric -StartTime $StartTime -EndTime $EndTime -BatchContext $context
DataEgressGiB      : 6.68875873088837E-06
DataIngressGiB     : 1.9485130906105E-05
EndTime            : 5/16/2016 12:30:00 AM
PoolId             : testpool1
StartTime          : 5/16/2016 12:00:00 AM
TotalCoreHours     : 8
VirtualMachineSize : standard_d4

DataEgressGiB      : 5.61587512493134E-06
DataIngressGiB     : 1.76150351762772E-05
EndTime            : 5/16/2016 12:30:00 AM
PoolId             : testpool2
StartTime          : 5/16/2016 12:00:00 AM
TotalCoreHours     : 12
VirtualMachineSize : standard_d4

DataEgressGiB      : 7.36676156520844E-06
DataIngressGiB     : 2.10804864764214E-05
EndTime            : 5/16/2016 1:00:00 AM
PoolId             : testpool1
StartTime          : 5/16/2016 12:30:00 AM
TotalCoreHours     : 7.99999999955555
VirtualMachineSize : standard_d4

DataEgressGiB      : 5.80586493015289E-06
DataIngressGiB     : 1.80602073669434E-05
EndTime            : 5/16/2016 1:00:00 AM
PoolId             : testpool2
StartTime          : 5/16/2016 12:30:00 AM
TotalCoreHours     : 11.9999999993333
VirtualMachineSize : standard_d4
```

<span data-ttu-id="98ab1-110">Первая команда создает ссылку на объект для учетной записи пакетной службы с именем ContosoBatchAccount с помощью **Get-AzBatchAccountKey**.</span><span class="sxs-lookup"><span data-stu-id="98ab1-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="98ab1-111">Команда сохраняет ссылку на этот объект в переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="98ab1-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="98ab1-112">Следующие две команды создают объекты **DateTime** с помощью командлета Get-Date.</span><span class="sxs-lookup"><span data-stu-id="98ab1-112">The next two commands create **DateTime** objects by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="98ab1-113">Команды хранят эти значения в переменных $StartTime и $EndTime, которые используются в финальной команде.</span><span class="sxs-lookup"><span data-stu-id="98ab1-113">The commands store these values in the $StartTime and $EndTime variables for use with the final command.</span></span>
<span data-ttu-id="98ab1-114">Последняя команда возвращает все метрики использования пула, агрегированные по пулам, через интервал времени между указанными временем начала и окончания.</span><span class="sxs-lookup"><span data-stu-id="98ab1-114">The final command returns all of the pool usage metrics, aggregated by pool, across time interval between the specified start and end times.</span></span>

### <span data-ttu-id="98ab1-115">Пример 2: Получение метрик использования пула с помощью фильтра</span><span class="sxs-lookup"><span data-stu-id="98ab1-115">Example 2: Get pool usage metrics by using a filter</span></span>
```
PS C:\>Get-AzBatchPoolUsageMetric -Filter "poolId eq 'ContosoPool'" -BatchContext $Context
DataEgressGiB      : 9.0496614575386E-06
DataIngressGiB     : 2.60043889284134E-05
EndTime            : 5/16/2016 5:30:00 PM
PoolId             : MyPool
StartTime          : 5/16/2016 5:00:00 PM
TotalCoreHours     : 12
VirtualMachineSize : standard_d4
```

<span data-ttu-id="98ab1-116">Эта команда возвращает метрики использования для пула с именем ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="98ab1-116">This command returns the usage metrics for pool named ContosoPool.</span></span>
<span data-ttu-id="98ab1-117">Команда задает строку фильтра для задания пула и использует то же значение $Context, что и в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="98ab1-117">The command specifies a filter string to specify that pool, and uses the same $Context value as the previous example.</span></span>

## <span data-ttu-id="98ab1-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="98ab1-118">PARAMETERS</span></span>

### <span data-ttu-id="98ab1-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="98ab1-119">-BatchContext</span></span>
<span data-ttu-id="98ab1-120">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="98ab1-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="98ab1-121">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="98ab1-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="98ab1-122">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKey, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="98ab1-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="98ab1-123">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="98ab1-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="98ab1-124">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="98ab1-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="98ab1-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98ab1-125">-DefaultProfile</span></span>
<span data-ttu-id="98ab1-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="98ab1-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98ab1-127">-EndTime</span><span class="sxs-lookup"><span data-stu-id="98ab1-127">-EndTime</span></span>
<span data-ttu-id="98ab1-128">Указывает конец интервала времени, для которого этот командлет получает метрики использования.</span><span class="sxs-lookup"><span data-stu-id="98ab1-128">Specifies the end of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="98ab1-129">Укажите время по крайней мере два часа раньше.</span><span class="sxs-lookup"><span data-stu-id="98ab1-129">Specify a time at least two hours earlier.</span></span>
<span data-ttu-id="98ab1-130">Если время окончания не задано, в этом командлете используется последний из доступных интервалов агрегатов.</span><span class="sxs-lookup"><span data-stu-id="98ab1-130">If you do not specify an end time, this cmdlet uses the last aggregation interval currently available.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98ab1-131">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="98ab1-131">-Filter</span></span>
<span data-ttu-id="98ab1-132">Задает предложение фильтра OData, которое используется для фильтрации метрик, возвращаемых этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="98ab1-132">Specifies an OData filter clause to use to filter the metrics that this cmdlet returns.</span></span>
<span data-ttu-id="98ab1-133">Единственным допустимым свойством **poolId** является строковое значение.</span><span class="sxs-lookup"><span data-stu-id="98ab1-133">The only valid property is **poolId** with a string value.</span></span>
<span data-ttu-id="98ab1-134">Возможны следующие операции: EQ, GE, gt, Le, lt, StartsWith.</span><span class="sxs-lookup"><span data-stu-id="98ab1-134">Possible operations are the following: eq, ge, gt, le, lt, startswith.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98ab1-135">-StartTime</span><span class="sxs-lookup"><span data-stu-id="98ab1-135">-StartTime</span></span>
<span data-ttu-id="98ab1-136">Задает начало интервала времени, в течение которого этот командлет получает метрики использования.</span><span class="sxs-lookup"><span data-stu-id="98ab1-136">Specifies the start of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="98ab1-137">Укажите время в интервале времени не менее двух и не более чем на полчаса.</span><span class="sxs-lookup"><span data-stu-id="98ab1-137">Specify a time at least two and a half hours earlier.</span></span>
<span data-ttu-id="98ab1-138">Если время начала не задано, в этом командлете используется последний из доступных интервалов агрегатов.</span><span class="sxs-lookup"><span data-stu-id="98ab1-138">If you do not specify a start time, this cmdlet uses the last aggregation interval currently available.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98ab1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98ab1-139">CommonParameters</span></span>
<span data-ttu-id="98ab1-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="98ab1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98ab1-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98ab1-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98ab1-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="98ab1-142">INPUTS</span></span>

### <span data-ttu-id="98ab1-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="98ab1-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="98ab1-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="98ab1-144">OUTPUTS</span></span>

### <span data-ttu-id="98ab1-145">Microsoft.Azure.Commands.BatCH. Models. PSPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="98ab1-145">Microsoft.Azure.Commands.Batch.Models.PSPoolUsageMetrics</span></span>

## <span data-ttu-id="98ab1-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="98ab1-146">NOTES</span></span>

## <span data-ttu-id="98ab1-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="98ab1-147">RELATED LINKS</span></span>

[<span data-ttu-id="98ab1-148">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="98ab1-148">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="98ab1-149">Get-AzBatchPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="98ab1-149">Get-AzBatchPoolStatistics</span></span>](./Get-AzBatchPoolStatistic.md)

[<span data-ttu-id="98ab1-150">Get-AzBatchJobStatistics</span><span class="sxs-lookup"><span data-stu-id="98ab1-150">Get-AzBatchJobStatistics</span></span>](./Get-AzBatchJobStatistic.md)
