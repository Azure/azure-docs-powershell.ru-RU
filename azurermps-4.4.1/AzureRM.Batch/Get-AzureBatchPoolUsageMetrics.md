---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 4B373447-3078-4C1F-932E-8337AB170DEB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolUsageMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolUsageMetrics.md
ms.openlocfilehash: 4f985859cb26372a6ffc68b8521d08033fdc6670
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570131"
---
# <span data-ttu-id="fbe3d-101">Get-AzureBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="fbe3d-101">Get-AzureBatchPoolUsageMetrics</span></span>

## <span data-ttu-id="fbe3d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fbe3d-102">SYNOPSIS</span></span>
<span data-ttu-id="fbe3d-103">Получает метрики использования пула для учетной записи пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="fbe3d-103">Gets pool usage metrics for a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fbe3d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fbe3d-104">SYNTAX</span></span>

```
Get-AzureBatchPoolUsageMetrics [-StartTime <DateTime>] [-EndTime <DateTime>] [-Filter <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbe3d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fbe3d-105">DESCRIPTION</span></span>
<span data-ttu-id="fbe3d-106">Командлет **Get-AzureBatchPoolUsageMetrics** получает метрики использования, агрегированные по пулам между отдельными интервалами времени для указанной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="fbe3d-106">The **Get-AzureBatchPoolUsageMetrics** cmdlet gets the usage metrics, aggregated by pool across individual time intervals, for the specified account.</span></span>
<span data-ttu-id="fbe3d-107">Вы можете получить статистику для определенного пула и для интервала времени.</span><span class="sxs-lookup"><span data-stu-id="fbe3d-107">You can get the statistics for a specific pool and for a time range.</span></span>

## <span data-ttu-id="fbe3d-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fbe3d-108">EXAMPLES</span></span>

### <span data-ttu-id="fbe3d-109">Пример 1: Получение метрик использования пула для диапазона времени</span><span class="sxs-lookup"><span data-stu-id="fbe3d-109">Example 1: Get pool usage metrics for a time range</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $StartTime = Get-Date -Date "2016-05-16 00:00:00Z"
PS C:\> $EndTime = Get-Date -Date "2016-05-16 01:00:00Z"
PS C:\> Get-AzureBatchPoolUsageMetrics -StartTime $StartTime -EndTime $EndTime -BatchContext $context
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

<span data-ttu-id="fbe3d-110">Первая команда создает ссылку на объект для учетной записи пакетной службы с именем ContosoBatchAccount с помощью **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="fbe3d-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="fbe3d-111">Команда сохраняет ссылку на этот объект в переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="fbe3d-111">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="fbe3d-112">Следующие две команды создают объекты **DateTime** с помощью командлета Get-Date.</span><span class="sxs-lookup"><span data-stu-id="fbe3d-112">The next two commands create **DateTime** objects by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="fbe3d-113">Команды хранят эти значения в переменных $StartTime и $EndTime, которые используются в финальной команде.</span><span class="sxs-lookup"><span data-stu-id="fbe3d-113">The commands store these values in the $StartTime and $EndTime variables for use with the final command.</span></span>

<span data-ttu-id="fbe3d-114">Последняя команда возвращает все метрики использования пула, агрегированные по пулам, через интервал времени между указанными временем начала и окончания.</span><span class="sxs-lookup"><span data-stu-id="fbe3d-114">The final command returns all of the pool usage metrics, aggregated by pool, across time interval between the specified start and end times.</span></span>

### <span data-ttu-id="fbe3d-115">Пример 2: Получение метрик использования пула с помощью фильтра</span><span class="sxs-lookup"><span data-stu-id="fbe3d-115">Example 2: Get pool usage metrics by using a filter</span></span>
```
PS C:\>Get-AzureBatchPoolUsageMetrics -Filter "poolId eq 'ContosoPool'" -BatchContext $Context
DataEgressGiB      : 9.0496614575386E-06
DataIngressGiB     : 2.60043889284134E-05
EndTime            : 5/16/2016 5:30:00 PM
PoolId             : MyPool
StartTime          : 5/16/2016 5:00:00 PM
TotalCoreHours     : 12
VirtualMachineSize : standard_d4
```

<span data-ttu-id="fbe3d-116">Эта команда возвращает метрики использования для пула с именем ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="fbe3d-116">This command returns the usage metrics for pool named ContosoPool.</span></span>
<span data-ttu-id="fbe3d-117">Команда задает строку фильтра для задания пула и использует то же значение $Context, что и в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="fbe3d-117">The command specifies a filter string to specify that pool, and uses the same $Context value as the previous example.</span></span>

## <span data-ttu-id="fbe3d-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fbe3d-118">PARAMETERS</span></span>

### <span data-ttu-id="fbe3d-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="fbe3d-119">-BatchContext</span></span>
<span data-ttu-id="fbe3d-120">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="fbe3d-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="fbe3d-121">Чтобы получить объект **BatchAccountContext** , содержащий клавиши доступа для вашей подписки, используйте командлет Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="fbe3d-121">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="fbe3d-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="fbe3d-122">-EndTime</span></span>
<span data-ttu-id="fbe3d-123">Указывает конец интервала времени, для которого этот командлет получает метрики использования.</span><span class="sxs-lookup"><span data-stu-id="fbe3d-123">Specifies the end of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="fbe3d-124">Укажите время по крайней мере два часа раньше.</span><span class="sxs-lookup"><span data-stu-id="fbe3d-124">Specify a time at least two hours earlier.</span></span>
<span data-ttu-id="fbe3d-125">Если время окончания не задано, в этом командлете используется последний из доступных интервалов агрегатов.</span><span class="sxs-lookup"><span data-stu-id="fbe3d-125">If you do not specify an end time, this cmdlet uses the last aggregation interval currently available.</span></span>

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

### <span data-ttu-id="fbe3d-126">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="fbe3d-126">-Filter</span></span>
<span data-ttu-id="fbe3d-127">Задает предложение фильтра OData, которое используется для фильтрации метрик, которые этот командлет retruns.</span><span class="sxs-lookup"><span data-stu-id="fbe3d-127">Specifies an OData filter clause to use to filter the metrics that this cmdlet retruns.</span></span>
<span data-ttu-id="fbe3d-128">Единственным допустимым свойством **poolId** является строковое значение.</span><span class="sxs-lookup"><span data-stu-id="fbe3d-128">The only valid property is **poolId** with a string value.</span></span>
<span data-ttu-id="fbe3d-129">Возможны следующие операции: EQ, GE, gt, Le, lt, StartsWith.</span><span class="sxs-lookup"><span data-stu-id="fbe3d-129">Possible operations are the following: eq, ge, gt, le, lt, startswith.</span></span>

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

### <span data-ttu-id="fbe3d-130">-StartTime</span><span class="sxs-lookup"><span data-stu-id="fbe3d-130">-StartTime</span></span>
<span data-ttu-id="fbe3d-131">Задает начало интервала времени, в течение которого этот командлет получает метрики использования.</span><span class="sxs-lookup"><span data-stu-id="fbe3d-131">Specifies the start of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="fbe3d-132">Укажите время в интервале времени не менее двух и не более чем на полчаса.</span><span class="sxs-lookup"><span data-stu-id="fbe3d-132">Specify a time at least two and a half hours earlier.</span></span>
<span data-ttu-id="fbe3d-133">Если время начала не задано, в этом командлете используется последний из доступных интервалов агрегатов.</span><span class="sxs-lookup"><span data-stu-id="fbe3d-133">If you do not specify a start time, this cmdlet uses the last aggregation interval currently available.</span></span>

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

### <span data-ttu-id="fbe3d-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbe3d-134">-DefaultProfile</span></span>
<span data-ttu-id="fbe3d-135">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fbe3d-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fbe3d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbe3d-136">CommonParameters</span></span>
<span data-ttu-id="fbe3d-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fbe3d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbe3d-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbe3d-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbe3d-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fbe3d-139">INPUTS</span></span>

### <span data-ttu-id="fbe3d-140">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="fbe3d-140">BatchAccountContext</span></span>
<span data-ttu-id="fbe3d-141">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="fbe3d-141">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="fbe3d-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fbe3d-142">OUTPUTS</span></span>

### <span data-ttu-id="fbe3d-143">PSPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="fbe3d-143">PSPoolUsageMetrics</span></span>

## <span data-ttu-id="fbe3d-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="fbe3d-144">NOTES</span></span>

## <span data-ttu-id="fbe3d-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fbe3d-145">RELATED LINKS</span></span>

[<span data-ttu-id="fbe3d-146">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="fbe3d-146">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="fbe3d-147">Get-AzureBatchPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="fbe3d-147">Get-AzureBatchPoolStatistics</span></span>](./Get-AzureBatchPoolStatistics.md)

[<span data-ttu-id="fbe3d-148">Get-AzureBatchJobStatistics</span><span class="sxs-lookup"><span data-stu-id="fbe3d-148">Get-AzureBatchJobStatistics</span></span>](./Get-AzureBatchJobStatistics.md)


