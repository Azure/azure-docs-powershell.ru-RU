---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjobpreparationandreleasetaskstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
ms.openlocfilehash: ffc89f298715f9e878bb3283c99e794f92662e84
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239392"
---
# <span data-ttu-id="1b692-101">Get-AzBatchJobPreparationAndReleaseTaskStatus</span><span class="sxs-lookup"><span data-stu-id="1b692-101">Get-AzBatchJobPreparationAndReleaseTaskStatus</span></span>

## <span data-ttu-id="1b692-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b692-102">SYNOPSIS</span></span>
<span data-ttu-id="1b692-103">Пакетная подготовка задания и освобождение состояния задачи.</span><span class="sxs-lookup"><span data-stu-id="1b692-103">Gets Batch job preparation and release task status.</span></span>

## <span data-ttu-id="1b692-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1b692-104">SYNTAX</span></span>

### <span data-ttu-id="1b692-105">ИД (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1b692-105">Id (Default)</span></span>
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-Id] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b692-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="1b692-106">InputObject</span></span>
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-InputObject] <PSCloudJob> [-Filter <String>]
 [-MaxCount <Int32>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b692-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b692-107">DESCRIPTION</span></span>
<span data-ttu-id="1b692-108">Для получения пакета задания и выпуска задания пакета в Azure возвращается cmdlet **Get-AzBatchJobPreparationAndReleaseTaskStatus.**</span><span class="sxs-lookup"><span data-stu-id="1b692-108">The **Get-AzBatchJobPreparationAndReleaseTaskStatus** cmdlet gets the Azure Batch job preparation and release task status for a Batch job.</span></span>
<span data-ttu-id="1b692-109">Для этого *cmdlet* необходимо предоставить параметр Id или **экземпляр PSCloudJob.**</span><span class="sxs-lookup"><span data-stu-id="1b692-109">You must supply the *Id* parameter or a **PSCloudJob** instance to this cmdlet.</span></span>

## <span data-ttu-id="1b692-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1b692-110">EXAMPLES</span></span>

### <span data-ttu-id="1b692-111">Пример 1. Подготовка задания и ее освобождение</span><span class="sxs-lookup"><span data-stu-id="1b692-111">Example 1: Get the job preparation and release status of a job</span></span>
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $Context -Id Test

ComputeNodeId                          : tvm-2316545714_1-20170613t201733z
ComputeNodeUrl                         : https://account.westus.batch.azure.com/pools/test/nodes/tvm-2316545714_1-20170613t201733z
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 : test
```

<span data-ttu-id="1b692-112">Эта команда получает подготовку задания и статус задания "Проверка".</span><span class="sxs-lookup"><span data-stu-id="1b692-112">This command gets the job preparation and release task status for job "Test".</span></span>
<span data-ttu-id="1b692-113">Используйте Get-AzBatchAccountKey для назначения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="1b692-113">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="1b692-114">Пример 2. Подготовка и освобождение задания с помощью фильтра и выбранного</span><span class="sxs-lookup"><span data-stu-id="1b692-114">Example 2: Get the job preparation and release status of a job with Filter and Select specified</span></span>
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $context -Id Test -Filter "nodeId eq 'tvm-2316545714_1-20170613t201733z'" -Select "jobPreparationTaskExecutionInfo"

ComputeNodeId                          :
ComputeNodeUrl                         :
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 :
```

<span data-ttu-id="1b692-115">Эта команда получает подготовку задания и статус выпуска задания "Проверка" на узле "tvm-2316545714_1-20170613t201733z" и с помощью предложения Select указывает только возврат сведений о jobPreparationTaskExecutionInformation.</span><span class="sxs-lookup"><span data-stu-id="1b692-115">This command gets the job preparation and release task status for job "Test" on node "tvm-2316545714_1-20170613t201733z" and uses the Select clause to specify to only return the JobPreparationTaskExecutionInformation information</span></span>

## <span data-ttu-id="1b692-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b692-116">PARAMETERS</span></span>

### <span data-ttu-id="1b692-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="1b692-117">-BatchContext</span></span>
<span data-ttu-id="1b692-118">Экземпляр BatchAccountContext, который используется при взаимодействии со службой batch.</span><span class="sxs-lookup"><span data-stu-id="1b692-118">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="1b692-119">Используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными клавишами доступа.</span><span class="sxs-lookup"><span data-stu-id="1b692-119">Use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>

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

### <span data-ttu-id="1b692-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b692-120">-DefaultProfile</span></span>
<span data-ttu-id="1b692-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1b692-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b692-122">-Развернуть</span><span class="sxs-lookup"><span data-stu-id="1b692-122">-Expand</span></span>
<span data-ttu-id="1b692-123">Указывает предложение развернуть протокол Open Data (OData).</span><span class="sxs-lookup"><span data-stu-id="1b692-123">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="1b692-124">Укажите значение этого параметра, чтобы получить связанные объекты основной сущности, которую вы получаете.</span><span class="sxs-lookup"><span data-stu-id="1b692-124">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="1b692-125">-Filter</span><span class="sxs-lookup"><span data-stu-id="1b692-125">-Filter</span></span>
<span data-ttu-id="1b692-126">Указывает предложение фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="1b692-126">Specifies an OData filter clause.</span></span>
<span data-ttu-id="1b692-127">Если не указать фильтр, этот cmdlet возвратит всю подготовку задания и отпустит состояние задачи.</span><span class="sxs-lookup"><span data-stu-id="1b692-127">If you do not specify a filter, this cmdlet returns all job preparation and release task status' for the job.</span></span>

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

### <span data-ttu-id="1b692-128">-Id</span><span class="sxs-lookup"><span data-stu-id="1b692-128">-Id</span></span>
<span data-ttu-id="1b692-129">Определяет ИД задания, для которого нужно получить задачи подготовки и освобождения.</span><span class="sxs-lookup"><span data-stu-id="1b692-129">Specifies the ID of the job whose preparation and release tasks should be retrieved.</span></span>
<span data-ttu-id="1b692-130">Поддиавные знаки указывать нельзя.</span><span class="sxs-lookup"><span data-stu-id="1b692-130">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="1b692-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1b692-131">-InputObject</span></span>
<span data-ttu-id="1b692-132">Указывает объект **PSCloudJob,** представляю который представляет задание, с целью подготовки и выпуска состояния задачи.</span><span class="sxs-lookup"><span data-stu-id="1b692-132">Specifies a **PSCloudJob** object that represents the job to get the preparation and release task status from.</span></span>
<span data-ttu-id="1b692-133">Чтобы получить объект **PSCloudJob,** используйте Get-AzBatchJob-код.</span><span class="sxs-lookup"><span data-stu-id="1b692-133">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="1b692-134">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="1b692-134">-MaxCount</span></span>
<span data-ttu-id="1b692-135">Указывает максимальное количество заданий для подготовки и освобождения от дел, которые нужно вернуть.</span><span class="sxs-lookup"><span data-stu-id="1b692-135">Specifies the maximum number of jobs preparation and release task status' to return.</span></span>
<span data-ttu-id="1b692-136">Если указать нулевое (ноль) или меньшее значение, для cmdlet не используется верхний предел.</span><span class="sxs-lookup"><span data-stu-id="1b692-136">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="1b692-137">Значение по умолчанию — 1000.</span><span class="sxs-lookup"><span data-stu-id="1b692-137">The default value is 1000.</span></span>

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

### <span data-ttu-id="1b692-138">-Select</span><span class="sxs-lookup"><span data-stu-id="1b692-138">-Select</span></span>
<span data-ttu-id="1b692-139">Указывает предложение выбора OData.</span><span class="sxs-lookup"><span data-stu-id="1b692-139">Specifies an OData select clause.</span></span>
<span data-ttu-id="1b692-140">Укажите значение для этого параметра, чтобы получить определенные свойства, а не все свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="1b692-140">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="1b692-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b692-141">CommonParameters</span></span>
<span data-ttu-id="1b692-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b692-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b692-143">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1b692-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b692-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1b692-144">INPUTS</span></span>

### <span data-ttu-id="1b692-145">Microsoft.Azure.Commands.Batch. Models.PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="1b692-145">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="1b692-146">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="1b692-146">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="1b692-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1b692-147">OUTPUTS</span></span>

### <span data-ttu-id="1b692-148">Microsoft.Azure.Commands.Batch. Models.PSJobPreparationAndReleaseTaskExecutionInformation</span><span class="sxs-lookup"><span data-stu-id="1b692-148">Microsoft.Azure.Commands.Batch.Models.PSJobPreparationAndReleaseTaskExecutionInformation</span></span>

## <span data-ttu-id="1b692-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1b692-149">NOTES</span></span>

## <span data-ttu-id="1b692-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1b692-150">RELATED LINKS</span></span>

[<span data-ttu-id="1b692-151">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="1b692-151">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="1b692-152">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="1b692-152">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
