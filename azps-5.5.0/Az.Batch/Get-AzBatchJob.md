---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 8BF49C4D-E7CD-4FD0-AFAC-9856239D24EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJob.md
ms.openlocfilehash: b0709c7b839ca992d415cd5ba9fff58e769120fb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239397"
---
# <span data-ttu-id="61ee9-101">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="61ee9-101">Get-AzBatchJob</span></span>

## <span data-ttu-id="61ee9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61ee9-102">SYNOPSIS</span></span>
<span data-ttu-id="61ee9-103">Пакетные задания для пакетной учетной записи или расписания заданий.</span><span class="sxs-lookup"><span data-stu-id="61ee9-103">Gets Batch jobs for a Batch account or job schedule.</span></span>

## <span data-ttu-id="61ee9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="61ee9-104">SYNTAX</span></span>

### <span data-ttu-id="61ee9-105">ODataFilter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="61ee9-105">ODataFilter (Default)</span></span>
```
Get-AzBatchJob [-JobScheduleId <String>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="61ee9-106">ИД</span><span class="sxs-lookup"><span data-stu-id="61ee9-106">Id</span></span>
```
Get-AzBatchJob [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61ee9-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="61ee9-107">ParentObject</span></span>
```
Get-AzBatchJob [[-JobSchedule] <PSCloudJobSchedule>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="61ee9-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="61ee9-108">DESCRIPTION</span></span>
<span data-ttu-id="61ee9-109">С **помощью cmdlet Get-AzBatchJob** можно получить задания пакета Azure для учетной записи Batch, заданной *параметром BatchAccountContext.*</span><span class="sxs-lookup"><span data-stu-id="61ee9-109">The **Get-AzBatchJob** cmdlet gets the Azure Batch jobs for the Batch account specified by the *BatchAccountContext* parameter.</span></span>
<span data-ttu-id="61ee9-110">С помощью *параметра Id* можно получить одно задание.</span><span class="sxs-lookup"><span data-stu-id="61ee9-110">You can use the *Id* parameter to get a single job.</span></span>
<span data-ttu-id="61ee9-111">С помощью параметра *Filter* можно получить задания, которые соответствуют фильтру OData.</span><span class="sxs-lookup"><span data-stu-id="61ee9-111">You can use the *Filter* parameter to get the jobs that match an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="61ee9-112">Если у вас есть код расписания задания или **экземпляр PSCloudJobSchedule,** этот cmdlet возвращает только задания для этого расписания.</span><span class="sxs-lookup"><span data-stu-id="61ee9-112">If you supply a job schedule ID or **PSCloudJobSchedule** instance, this cmdlet returns only the jobs for that job schedule.</span></span>

## <span data-ttu-id="61ee9-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="61ee9-113">EXAMPLES</span></span>

### <span data-ttu-id="61ee9-114">Пример 1. Пакетное задание по ИД</span><span class="sxs-lookup"><span data-stu-id="61ee9-114">Example 1: Get a Batch job by ID</span></span>
```
PS C:\>Get-AzBatchJob -Id "Job01" -BatchContext $Context
CommonEnvironmentSettings   :
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
CreationTime                : 7/25/2015 9:12:07 PM
DisplayName                 :
ETag                        : 0x8D29535B2941439
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobExecutionInformation
Id                          : Job01
JobManagerTask              :
JobPreparationTask          :
JobReleaseTask              :
LastModified                : 7/25/2015 9:12:07 PM
Metadata                    :
PoolInformation             : Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
PreviousState               :
PreviousStateTransitionTime :
Priority                    : 0
State                       : Active
StateTransitionTime         : 7/25/2015 9:12:07 PM
Statistics                  :
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job01
```

<span data-ttu-id="61ee9-115">Эта команда получает задание, у которое есть задание "ИД01".</span><span class="sxs-lookup"><span data-stu-id="61ee9-115">This command gets the job that has the ID Job01.</span></span>
<span data-ttu-id="61ee9-116">Используйте Get-AzBatchAccountKey для назначения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="61ee9-116">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="61ee9-117">Пример 2. Поиск всех активных заданий для расписания заданий</span><span class="sxs-lookup"><span data-stu-id="61ee9-117">Example 2: Get all active jobs for a job schedule</span></span>
```
PS C:\>Get-AzBatchJob -JobScheduleId "JobSchedule27" -Filter "state eq 'active'" -BatchContext $Context
CommonEnvironmentSettings   :
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
CreationTime                : 7/25/2015 9:15:44 PM
DisplayName                 :
ETag                        : 0x8D2953633DD13E1
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobExecutionInformation
Id                          : JobSchedule27:job-1
JobManagerTask              :
JobPreparationTask          :
JobReleaseTask              :
LastModified                : 7/25/2015 9:15:44 PM
Metadata                    :
PoolInformation             : Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
PreviousState               :
PreviousStateTransitionTime :
Priority                    : 0
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:44 PM
Statistics                  :
Url                         : https://pfuller.westus.batch.azure.com/jobs/JobSchedule27:job-1
```

<span data-ttu-id="61ee9-118">Эта команда возвращает активные задания для расписания заданий с расписанием заданий ID JobSchedule27.</span><span class="sxs-lookup"><span data-stu-id="61ee9-118">This command gets the active jobs for the job schedule that has the ID JobSchedule27.</span></span>

### <span data-ttu-id="61ee9-119">Пример 3. Получает все задания в соответствии с расписанием заданий с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="61ee9-119">Example 3: Gets all jobs under a job schedule by using the pipeline</span></span>
```
PS C:\>Get-AzBatchJobSchedule -Id "JobSchedule27" -BatchContext $Context | Get-AzBatchJob -BatchContext $Context
CommonEnvironmentSettings   :
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
CreationTime                : 7/25/2015 9:15:44 PM
DisplayName                 :
ETag                        : 0x8D2953633DD13E1
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobExecutionInformation
Id                          : JobSchedule27:job-1
JobManagerTask              :
JobPreparationTask          :
JobReleaseTask              :
LastModified                : 7/25/2015 9:15:44 PM
Metadata                    :
PoolInformation             : Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
PreviousState               :
PreviousStateTransitionTime :
Priority                    : 0
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:44 PM
Statistics                  :
Url                         : https://pfuller.westus.batch.azure.com/jobs/JobSchedule27:job-1
```

<span data-ttu-id="61ee9-120">Эта команда получает расписание задания с расписанием и расписанием задания с помощью Get-AzBatchJobSchedule календаря.</span><span class="sxs-lookup"><span data-stu-id="61ee9-120">This command gets the job schedule that has the ID JobSchedule27 by using the Get-AzBatchJobSchedule cmdlet.</span></span>
<span data-ttu-id="61ee9-121">Эта команда передает расписание задания текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="61ee9-121">The command passes that job schedule to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="61ee9-122">Команда получает все задания для этого расписания заданий.</span><span class="sxs-lookup"><span data-stu-id="61ee9-122">The command gets all jobs for that job schedule.</span></span>

## <span data-ttu-id="61ee9-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61ee9-123">PARAMETERS</span></span>

### <span data-ttu-id="61ee9-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="61ee9-124">-BatchContext</span></span>
<span data-ttu-id="61ee9-125">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="61ee9-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="61ee9-126">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой batchy будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="61ee9-126">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="61ee9-127">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="61ee9-127">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="61ee9-128">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="61ee9-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="61ee9-129">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="61ee9-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="61ee9-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61ee9-130">-DefaultProfile</span></span>
<span data-ttu-id="61ee9-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="61ee9-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61ee9-132">-Развернуть</span><span class="sxs-lookup"><span data-stu-id="61ee9-132">-Expand</span></span>
<span data-ttu-id="61ee9-133">Указывает предложение развернуть протокол Open Data (OData).</span><span class="sxs-lookup"><span data-stu-id="61ee9-133">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="61ee9-134">Укажите значение этого параметра, чтобы получить связанные объекты основной сущности, которую вы получаете.</span><span class="sxs-lookup"><span data-stu-id="61ee9-134">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="61ee9-135">-Filter</span><span class="sxs-lookup"><span data-stu-id="61ee9-135">-Filter</span></span>
<span data-ttu-id="61ee9-136">Указывает предложение фильтра OData для заданий.</span><span class="sxs-lookup"><span data-stu-id="61ee9-136">Specifies an OData filter clause for jobs.</span></span>
<span data-ttu-id="61ee9-137">Если не указать фильтр, этот cmdlet возвращает все задания для учетной записи пакета или расписания заданий.</span><span class="sxs-lookup"><span data-stu-id="61ee9-137">If you do not specify a filter, this cmdlet returns all jobs for the Batch account or job schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter, ParentObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61ee9-138">-Id</span><span class="sxs-lookup"><span data-stu-id="61ee9-138">-Id</span></span>
<span data-ttu-id="61ee9-139">Определяет код задания, которое получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61ee9-139">Specifies the ID of the job that this cmdlet gets.</span></span>
<span data-ttu-id="61ee9-140">Поддиавные знаки указывать нельзя.</span><span class="sxs-lookup"><span data-stu-id="61ee9-140">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61ee9-141">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="61ee9-141">-JobSchedule</span></span>
<span data-ttu-id="61ee9-142">Указывает объект **PSCloudJobSchedule,** который представляет расписание заданий, которое содержит задания.</span><span class="sxs-lookup"><span data-stu-id="61ee9-142">Specifies a **PSCloudJobSchedule** object that represents the job schedule which contains the jobs.</span></span>
<span data-ttu-id="61ee9-143">Чтобы получить объект **PSCloudJobSchedule,** используйте Get-AzBatchJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="61ee9-143">To obtain a **PSCloudJobSchedule** object, use the Get-AzBatchJobSchedule cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61ee9-144">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="61ee9-144">-JobScheduleId</span></span>
<span data-ttu-id="61ee9-145">Определяет ИД расписания заданий, который содержит задания.</span><span class="sxs-lookup"><span data-stu-id="61ee9-145">Specifies the ID of the job schedule which contains the jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61ee9-146">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="61ee9-146">-MaxCount</span></span>
<span data-ttu-id="61ee9-147">Указывает максимальное количество возвращаемых заданий.</span><span class="sxs-lookup"><span data-stu-id="61ee9-147">Specifies the maximum number of jobs to return.</span></span>
<span data-ttu-id="61ee9-148">Если указать нулевое (ноль) или меньшее значение, для cmdlet не используется верхний предел.</span><span class="sxs-lookup"><span data-stu-id="61ee9-148">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="61ee9-149">Значение по умолчанию — 1000.</span><span class="sxs-lookup"><span data-stu-id="61ee9-149">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter, ParentObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61ee9-150">-Select</span><span class="sxs-lookup"><span data-stu-id="61ee9-150">-Select</span></span>
<span data-ttu-id="61ee9-151">Указывает предложение выбора OData.</span><span class="sxs-lookup"><span data-stu-id="61ee9-151">Specifies an OData select clause.</span></span>
<span data-ttu-id="61ee9-152">Укажите значение для этого параметра, чтобы получить определенные свойства, а не все свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="61ee9-152">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="61ee9-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61ee9-153">CommonParameters</span></span>
<span data-ttu-id="61ee9-154">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61ee9-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61ee9-155">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="61ee9-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61ee9-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="61ee9-156">INPUTS</span></span>

### <span data-ttu-id="61ee9-157">System.String</span><span class="sxs-lookup"><span data-stu-id="61ee9-157">System.String</span></span>

### <span data-ttu-id="61ee9-158">Microsoft.Azure.Commands.Batch. Models.PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="61ee9-158">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

### <span data-ttu-id="61ee9-159">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="61ee9-159">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="61ee9-160">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="61ee9-160">OUTPUTS</span></span>

### <span data-ttu-id="61ee9-161">Microsoft.Azure.Commands.Batch. Models.PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="61ee9-161">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

## <span data-ttu-id="61ee9-162">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="61ee9-162">NOTES</span></span>

## <span data-ttu-id="61ee9-163">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="61ee9-163">RELATED LINKS</span></span>

[<span data-ttu-id="61ee9-164">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="61ee9-164">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="61ee9-165">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="61ee9-165">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="61ee9-166">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="61ee9-166">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="61ee9-167">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="61ee9-167">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="61ee9-168">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="61ee9-168">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="61ee9-169">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="61ee9-169">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="61ee9-170">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="61ee9-170">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="61ee9-171">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="61ee9-171">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
