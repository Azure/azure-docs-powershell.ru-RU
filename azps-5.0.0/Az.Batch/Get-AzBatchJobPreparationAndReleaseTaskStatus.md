---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjobpreparationandreleasetaskstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
ms.openlocfilehash: ffc89f298715f9e878bb3283c99e794f92662e84
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248764"
---
# <span data-ttu-id="23268-101">Get-AzBatchJobPreparationAndReleaseTaskStatus</span><span class="sxs-lookup"><span data-stu-id="23268-101">Get-AzBatchJobPreparationAndReleaseTaskStatus</span></span>

## <span data-ttu-id="23268-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="23268-102">SYNOPSIS</span></span>
<span data-ttu-id="23268-103">Возвращает состояние подготовки пакетного задания и выпуск задачи.</span><span class="sxs-lookup"><span data-stu-id="23268-103">Gets Batch job preparation and release task status.</span></span>

## <span data-ttu-id="23268-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="23268-104">SYNTAX</span></span>

### <span data-ttu-id="23268-105">ID (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="23268-105">Id (Default)</span></span>
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-Id] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23268-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="23268-106">InputObject</span></span>
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-InputObject] <PSCloudJob> [-Filter <String>]
 [-MaxCount <Int32>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23268-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="23268-107">DESCRIPTION</span></span>
<span data-ttu-id="23268-108">Командлет **Get-AzBatchJobPreparationAndReleaseTaskStatus** получает статус подготовки пакетного задания Azure и состояние задачи выпуска для пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="23268-108">The **Get-AzBatchJobPreparationAndReleaseTaskStatus** cmdlet gets the Azure Batch job preparation and release task status for a Batch job.</span></span>
<span data-ttu-id="23268-109">Для этого командлета необходимо указать параметр *ID* или экземпляр **PSCloudJob** .</span><span class="sxs-lookup"><span data-stu-id="23268-109">You must supply the *Id* parameter or a **PSCloudJob** instance to this cmdlet.</span></span>

## <span data-ttu-id="23268-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="23268-110">EXAMPLES</span></span>

### <span data-ttu-id="23268-111">Пример 1: получение сведений о подготовке задания и его выпуске</span><span class="sxs-lookup"><span data-stu-id="23268-111">Example 1: Get the job preparation and release status of a job</span></span>
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $Context -Id Test

ComputeNodeId                          : tvm-2316545714_1-20170613t201733z
ComputeNodeUrl                         : https://account.westus.batch.azure.com/pools/test/nodes/tvm-2316545714_1-20170613t201733z
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 : test
```

<span data-ttu-id="23268-112">Эта команда получает состояние задачи подготовки и выпуска для задания "тест".</span><span class="sxs-lookup"><span data-stu-id="23268-112">This command gets the job preparation and release task status for job "Test".</span></span>
<span data-ttu-id="23268-113">Используйте командлет Get-AzBatchAccountKey для присвоения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="23268-113">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="23268-114">Пример 2: получение сведений о подготовке и выпуске задания с фильтром и выбор указанного</span><span class="sxs-lookup"><span data-stu-id="23268-114">Example 2: Get the job preparation and release status of a job with Filter and Select specified</span></span>
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $context -Id Test -Filter "nodeId eq 'tvm-2316545714_1-20170613t201733z'" -Select "jobPreparationTaskExecutionInfo"

ComputeNodeId                          :
ComputeNodeUrl                         :
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 :
```

<span data-ttu-id="23268-115">Эта команда получает состояние задачи подготовки и освобождения для задания "тест" на узле "TVM-2316545714_1-20170613t201733z" и использует предложение SELECT, чтобы указать, что нужно возвращать только сведения о JobPreparationTaskExecutionInformation</span><span class="sxs-lookup"><span data-stu-id="23268-115">This command gets the job preparation and release task status for job "Test" on node "tvm-2316545714_1-20170613t201733z" and uses the Select clause to specify to only return the JobPreparationTaskExecutionInformation information</span></span>

## <span data-ttu-id="23268-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="23268-116">PARAMETERS</span></span>

### <span data-ttu-id="23268-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="23268-117">-BatchContext</span></span>
<span data-ttu-id="23268-118">Экземпляр BatchAccountContext, который будет использоваться при взаимодействии со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="23268-118">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="23268-119">Используйте командлет Get-AzBatchAccountKey, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="23268-119">Use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>

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

### <span data-ttu-id="23268-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23268-120">-DefaultProfile</span></span>
<span data-ttu-id="23268-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="23268-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23268-122">-Expand</span><span class="sxs-lookup"><span data-stu-id="23268-122">-Expand</span></span>
<span data-ttu-id="23268-123">Указывает предложение развертывания протокола Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="23268-123">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="23268-124">Укажите значение этого параметра, чтобы получить связанные сущности от основной сущности, которые вы получаете.</span><span class="sxs-lookup"><span data-stu-id="23268-124">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="23268-125">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="23268-125">-Filter</span></span>
<span data-ttu-id="23268-126">Задает предложение фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="23268-126">Specifies an OData filter clause.</span></span>
<span data-ttu-id="23268-127">Если вы не укажете фильтр, этот командлет возвращает состояние задачи "подготовка" и "выпуск" для задания.</span><span class="sxs-lookup"><span data-stu-id="23268-127">If you do not specify a filter, this cmdlet returns all job preparation and release task status' for the job.</span></span>

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

### <span data-ttu-id="23268-128">-ID</span><span class="sxs-lookup"><span data-stu-id="23268-128">-Id</span></span>
<span data-ttu-id="23268-129">Указывает идентификатор задания, для которого требуется получить задачи подготовки и выпуска.</span><span class="sxs-lookup"><span data-stu-id="23268-129">Specifies the ID of the job whose preparation and release tasks should be retrieved.</span></span>
<span data-ttu-id="23268-130">Подстановочные знаки указывать нельзя.</span><span class="sxs-lookup"><span data-stu-id="23268-130">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23268-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23268-131">-InputObject</span></span>
<span data-ttu-id="23268-132">Указывает объект **PSCloudJob** , который представляет задание для получения состояния задачи подготовки и выпуска.</span><span class="sxs-lookup"><span data-stu-id="23268-132">Specifies a **PSCloudJob** object that represents the job to get the preparation and release task status from.</span></span>
<span data-ttu-id="23268-133">Чтобы получить объект **PSCloudJob** , используйте командлет Get-AzBatchJob.</span><span class="sxs-lookup"><span data-stu-id="23268-133">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23268-134">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="23268-134">-MaxCount</span></span>
<span data-ttu-id="23268-135">Задает максимальное количество возвращаемых заданий и состояние задачи "выпустить".</span><span class="sxs-lookup"><span data-stu-id="23268-135">Specifies the maximum number of jobs preparation and release task status' to return.</span></span>
<span data-ttu-id="23268-136">Если вы задаете нулевое значение (0) или меньше, в командлете не используется верхний предел.</span><span class="sxs-lookup"><span data-stu-id="23268-136">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="23268-137">Значение по умолчанию — 1000.</span><span class="sxs-lookup"><span data-stu-id="23268-137">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23268-138">-SELECT</span><span class="sxs-lookup"><span data-stu-id="23268-138">-Select</span></span>
<span data-ttu-id="23268-139">Задает предложение SELECT OData.</span><span class="sxs-lookup"><span data-stu-id="23268-139">Specifies an OData select clause.</span></span>
<span data-ttu-id="23268-140">Укажите значение этого параметра, чтобы получить конкретные свойства, а не все свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="23268-140">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="23268-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23268-141">CommonParameters</span></span>
<span data-ttu-id="23268-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="23268-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23268-143">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23268-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23268-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="23268-144">INPUTS</span></span>

### <span data-ttu-id="23268-145">Microsoft.Azure.Commands.BatCH. Models. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="23268-145">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="23268-146">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="23268-146">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="23268-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="23268-147">OUTPUTS</span></span>

### <span data-ttu-id="23268-148">Microsoft.Azure.Commands.BatCH. Models. PSJobPreparationAndReleaseTaskExecutionInformation</span><span class="sxs-lookup"><span data-stu-id="23268-148">Microsoft.Azure.Commands.Batch.Models.PSJobPreparationAndReleaseTaskExecutionInformation</span></span>

## <span data-ttu-id="23268-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="23268-149">NOTES</span></span>

## <span data-ttu-id="23268-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="23268-150">RELATED LINKS</span></span>

[<span data-ttu-id="23268-151">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="23268-151">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="23268-152">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="23268-152">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)