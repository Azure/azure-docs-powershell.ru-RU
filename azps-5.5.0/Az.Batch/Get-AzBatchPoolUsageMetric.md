---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 4B373447-3078-4C1F-932E-8337AB170DEB
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchpoolusagemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolUsageMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolUsageMetric.md
ms.openlocfilehash: 1700e20318a502f32386638f94a9c5c86c271d7d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239306"
---
# <span data-ttu-id="f4e25-101">Get-AzBatchPoolUsageMetric</span><span class="sxs-lookup"><span data-stu-id="f4e25-101">Get-AzBatchPoolUsageMetric</span></span>

## <span data-ttu-id="f4e25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4e25-102">SYNOPSIS</span></span>
<span data-ttu-id="f4e25-103">Возвращает показатели использования пула для пакетной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f4e25-103">Gets pool usage metrics for a Batch account.</span></span>

## <span data-ttu-id="f4e25-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f4e25-104">SYNTAX</span></span>

```
Get-AzBatchPoolUsageMetric [-StartTime <DateTime>] [-EndTime <DateTime>] [-Filter <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4e25-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4e25-105">DESCRIPTION</span></span>
<span data-ttu-id="f4e25-106">Для указанной учетной записи с помощью cmdlet **Get-AzBatchPoolUsageMetric** метрики использования, совокупные по пулу за отдельные интервалы времени.</span><span class="sxs-lookup"><span data-stu-id="f4e25-106">The **Get-AzBatchPoolUsageMetric** cmdlet gets the usage metrics, aggregated by pool across individual time intervals, for the specified account.</span></span>
<span data-ttu-id="f4e25-107">Вы можете получить статистику по определенному пулу и за определенный диапазон времени.</span><span class="sxs-lookup"><span data-stu-id="f4e25-107">You can get the statistics for a specific pool and for a time range.</span></span>

## <span data-ttu-id="f4e25-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f4e25-108">EXAMPLES</span></span>

### <span data-ttu-id="f4e25-109">Пример 1. Метрики использования пула для диапазона времени</span><span class="sxs-lookup"><span data-stu-id="f4e25-109">Example 1: Get pool usage metrics for a time range</span></span>
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

<span data-ttu-id="f4e25-110">Первая команда создает ссылку на ключи учетных записей для пакетной учетной записи ContosoBatchAccount с помощью **Get-AzBatchAccountKey.**</span><span class="sxs-lookup"><span data-stu-id="f4e25-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="f4e25-111">Эта ссылка на объект сохраняется в переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="f4e25-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="f4e25-112">Следующие две команды создают объекты **даты и** времени с помощью Get-Date командлета.</span><span class="sxs-lookup"><span data-stu-id="f4e25-112">The next two commands create **DateTime** objects by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="f4e25-113">Эти значения сохраняются в $StartTime и $EndTime для использования с конечной командой.</span><span class="sxs-lookup"><span data-stu-id="f4e25-113">The commands store these values in the $StartTime and $EndTime variables for use with the final command.</span></span>
<span data-ttu-id="f4e25-114">Конечная команда возвращает все показатели использования пула, совокупные в пуле за определенный интервал времени между указанным временем начала и окончания.</span><span class="sxs-lookup"><span data-stu-id="f4e25-114">The final command returns all of the pool usage metrics, aggregated by pool, across time interval between the specified start and end times.</span></span>

### <span data-ttu-id="f4e25-115">Пример 2. Метрики использования пула с помощью фильтра</span><span class="sxs-lookup"><span data-stu-id="f4e25-115">Example 2: Get pool usage metrics by using a filter</span></span>
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

<span data-ttu-id="f4e25-116">Эта команда возвращает показатели использования для пула с именем ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="f4e25-116">This command returns the usage metrics for pool named ContosoPool.</span></span>
<span data-ttu-id="f4e25-117">Эта команда указывает строку фильтра, определяемую пулом, и использует то же $Context, что и в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="f4e25-117">The command specifies a filter string to specify that pool, and uses the same $Context value as the previous example.</span></span>

## <span data-ttu-id="f4e25-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4e25-118">PARAMETERS</span></span>

### <span data-ttu-id="f4e25-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f4e25-119">-BatchContext</span></span>
<span data-ttu-id="f4e25-120">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="f4e25-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f4e25-121">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой batchy будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f4e25-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f4e25-122">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="f4e25-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f4e25-123">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f4e25-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f4e25-124">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="f4e25-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="f4e25-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4e25-125">-DefaultProfile</span></span>
<span data-ttu-id="f4e25-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f4e25-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4e25-127">-EndTime</span><span class="sxs-lookup"><span data-stu-id="f4e25-127">-EndTime</span></span>
<span data-ttu-id="f4e25-128">Определяет конец диапазона времени, для которого этот cmdlet получает метрики использования.</span><span class="sxs-lookup"><span data-stu-id="f4e25-128">Specifies the end of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="f4e25-129">Укажите время по крайней мере на два часа раньше.</span><span class="sxs-lookup"><span data-stu-id="f4e25-129">Specify a time at least two hours earlier.</span></span>
<span data-ttu-id="f4e25-130">Если не указать время окончания, этот cmdlet использует последний доступный в настоящее время интервал агрегирования.</span><span class="sxs-lookup"><span data-stu-id="f4e25-130">If you do not specify an end time, this cmdlet uses the last aggregation interval currently available.</span></span>

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

### <span data-ttu-id="f4e25-131">-Filter</span><span class="sxs-lookup"><span data-stu-id="f4e25-131">-Filter</span></span>
<span data-ttu-id="f4e25-132">Указывает предложение фильтра OData, которое будет использовать для фильтрации метрики, возвращаемой этим cmdletом.</span><span class="sxs-lookup"><span data-stu-id="f4e25-132">Specifies an OData filter clause to use to filter the metrics that this cmdlet returns.</span></span>
<span data-ttu-id="f4e25-133">Допустимым свойством является **poolId со** строковой строкой.</span><span class="sxs-lookup"><span data-stu-id="f4e25-133">The only valid property is **poolId** with a string value.</span></span>
<span data-ttu-id="f4e25-134">Возможные операции: eq, ge, gt, le, lt, startswith.</span><span class="sxs-lookup"><span data-stu-id="f4e25-134">Possible operations are the following: eq, ge, gt, le, lt, startswith.</span></span>

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

### <span data-ttu-id="f4e25-135">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f4e25-135">-StartTime</span></span>
<span data-ttu-id="f4e25-136">Определяет начало диапазона времени, для которого этот cmdlet получает метрики использования.</span><span class="sxs-lookup"><span data-stu-id="f4e25-136">Specifies the start of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="f4e25-137">Укажите время по крайней мере на два с 1,5 часа раньше.</span><span class="sxs-lookup"><span data-stu-id="f4e25-137">Specify a time at least two and a half hours earlier.</span></span>
<span data-ttu-id="f4e25-138">Если время начала не за указано, используется последний доступный в данный момент интервал агрегирования.</span><span class="sxs-lookup"><span data-stu-id="f4e25-138">If you do not specify a start time, this cmdlet uses the last aggregation interval currently available.</span></span>

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

### <span data-ttu-id="f4e25-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4e25-139">CommonParameters</span></span>
<span data-ttu-id="f4e25-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4e25-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4e25-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f4e25-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4e25-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f4e25-142">INPUTS</span></span>

### <span data-ttu-id="f4e25-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f4e25-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="f4e25-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f4e25-144">OUTPUTS</span></span>

### <span data-ttu-id="f4e25-145">Microsoft.Azure.Commands.Batch. Models.PSPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="f4e25-145">Microsoft.Azure.Commands.Batch.Models.PSPoolUsageMetrics</span></span>

## <span data-ttu-id="f4e25-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f4e25-146">NOTES</span></span>

## <span data-ttu-id="f4e25-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f4e25-147">RELATED LINKS</span></span>

[<span data-ttu-id="f4e25-148">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="f4e25-148">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="f4e25-149">Get-AzBatchPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="f4e25-149">Get-AzBatchPoolStatistics</span></span>](./Get-AzBatchPoolStatistic.md)

[<span data-ttu-id="f4e25-150">Get-AzBatchJobStatistics</span><span class="sxs-lookup"><span data-stu-id="f4e25-150">Get-AzBatchJobStatistics</span></span>](./Get-AzBatchJobStatistic.md)
