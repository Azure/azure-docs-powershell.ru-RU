---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 4B5FE41A-090B-4859-B021-05CF0A8B7882
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTask.md
ms.openlocfilehash: 214ee3b030757da9acf632b2768a94b1ab026cc6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012723"
---
# <span data-ttu-id="82aa2-101">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="82aa2-101">Get-AzBatchTask</span></span>

## <span data-ttu-id="82aa2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82aa2-102">SYNOPSIS</span></span>
<span data-ttu-id="82aa2-103">Получает пакетные задачи для задания.</span><span class="sxs-lookup"><span data-stu-id="82aa2-103">Gets the Batch tasks for a job.</span></span>

## <span data-ttu-id="82aa2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="82aa2-104">SYNTAX</span></span>

### <span data-ttu-id="82aa2-105">ODataFilter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="82aa2-105">ODataFilter (Default)</span></span>
```
Get-AzBatchTask [-JobId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82aa2-106">ИД</span><span class="sxs-lookup"><span data-stu-id="82aa2-106">Id</span></span>
```
Get-AzBatchTask [-JobId] <String> [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82aa2-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="82aa2-107">ParentObject</span></span>
```
Get-AzBatchTask [[-Job] <PSCloudJob>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="82aa2-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="82aa2-108">DESCRIPTION</span></span>
<span data-ttu-id="82aa2-109">Для **выполнения пакетного** задания с его использованием получается пакетные задачи Azure.</span><span class="sxs-lookup"><span data-stu-id="82aa2-109">The **Get-AzBatchTask** cmdlet gets Azure Batch tasks for a Batch job.</span></span>
<span data-ttu-id="82aa2-110">Задание можно указать с помощью *параметров JobId* и *JobId.*</span><span class="sxs-lookup"><span data-stu-id="82aa2-110">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="82aa2-111">Чтобы получить одну задачу, укажите параметр *"ИД".*</span><span class="sxs-lookup"><span data-stu-id="82aa2-111">To get a single task, specify the *Id* parameter.</span></span>
<span data-ttu-id="82aa2-112">Вы можете указать параметр *Filter,* чтобы получить задачи, которые соответствуют фильтру OData.</span><span class="sxs-lookup"><span data-stu-id="82aa2-112">You can specify the *Filter* parameter to get the tasks that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="82aa2-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="82aa2-113">EXAMPLES</span></span>

### <span data-ttu-id="82aa2-114">Пример 1. Получить задачу по ИД</span><span class="sxs-lookup"><span data-stu-id="82aa2-114">Example 1: Get a task by ID</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job01" -Id "Task03" -BatchContext $Context
AffinityInformation         :
CommandLine                 : cmd /c dir /s
ComputeNodeInformation      : Microsoft.Azure.Commands.Batch.Models.PSComputeNodeInformation
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
CreationTime                : 7/25/2015 11:24:52 PM
DisplayName                 :
EnvironmentSettings         :
ETag                        : 0x8D295483E08BD9D
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSTaskExecutionInformation
Id                          : Task03
LastModified                : 7/25/2015 11:24:52 PM
PreviousState               : Running
PreviousStateTransitionTime : 7/25/2015 11:24:59 PM
ResourceFiles               :
RunElevated                 : False
State                       : Completed
StateTransitionTime         : 7/25/2015 11:24:59 PM
Statistics                  :
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job01/tasks/Task03
```

<span data-ttu-id="82aa2-115">Эта команда получает задачу с ИД задачи03 в рамках задания01.</span><span class="sxs-lookup"><span data-stu-id="82aa2-115">This command gets the task with ID Task03 under job Job01.</span></span>
<span data-ttu-id="82aa2-116">Используйте Get-AzBatchAccountKey для назначения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="82aa2-116">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="82aa2-117">Пример 2. Получить все завершенные задачи из определенного задания</span><span class="sxs-lookup"><span data-stu-id="82aa2-117">Example 2: Get all completed tasks from a specified job</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job02" -Filter "state eq 'completed'" -BatchContext $Context
AffinityInformation         :
CommandLine                 : cmd /c dir /s
ComputeNodeInformation      : Microsoft.Azure.Commands.Batch.Models.PSComputeNodeInformation
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
CreationTime                : 3/24/2015 10:21:51 PM
EnvironmentSettings         :
ETag                        : 0x8D295483E08BD9D
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSTaskExecutionInformation
Id                          : Task17
LastModified                : 3/24/2015 10:21:51 PM
PreviousState               : Running
PreviousStateTransitionTime : 3/24/2015 10:22:00 PM
ResourceFiles               :
RunElevated                 : False
State                       : Completed
StateTransitionTime         : 3/24/2015 10:22:00 PM
Statistics                  :
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job02/tasks/Task17

AffinityInformation         :
CommandLine                 : cmd /c echo hello > newFile.txt
ComputeNodeInformation      : Microsoft.Azure.Commands.Batch.Models.PSComputeNodeInformation
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
CreationTime                : 3/24/2015 10:21:51 PM
EnvironmentSettings         :
ETag                        : 0x8D295483E08BD9D
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSTaskExecutionInformation
Id                          : Task27
LastModified                : 3/24/2015 10:23:35 PM
PreviousState               : Running
PreviousStateTransitionTime : 3/24/2015 10:23:37 PM
ResourceFiles               :
RunElevated                 : True
State                       : Completed
StateTransitionTime         : 3/24/2015 10:23:37 PM
Statistics                  :
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job02/tasks/Task27
```

<span data-ttu-id="82aa2-118">Эта команда получает завершенные задачи из задания с заданием "ИД02".</span><span class="sxs-lookup"><span data-stu-id="82aa2-118">This command gets the completed tasks from the job that has the ID Job02.</span></span>

## <span data-ttu-id="82aa2-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82aa2-119">PARAMETERS</span></span>

### <span data-ttu-id="82aa2-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="82aa2-120">-BatchContext</span></span>
<span data-ttu-id="82aa2-121">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="82aa2-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="82aa2-122">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой batchy будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="82aa2-122">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="82aa2-123">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="82aa2-123">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="82aa2-124">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="82aa2-124">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="82aa2-125">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="82aa2-125">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="82aa2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82aa2-126">-DefaultProfile</span></span>
<span data-ttu-id="82aa2-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="82aa2-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82aa2-128">-Развернуть</span><span class="sxs-lookup"><span data-stu-id="82aa2-128">-Expand</span></span>
<span data-ttu-id="82aa2-129">Указывает предложение для расширения OData.</span><span class="sxs-lookup"><span data-stu-id="82aa2-129">Specifies an OData expand clause.</span></span>
<span data-ttu-id="82aa2-130">Укажите значение этого параметра, чтобы получить связанные объекты основного объекта, которые нужно получить.</span><span class="sxs-lookup"><span data-stu-id="82aa2-130">Specify a value for this parameter to get associated entities of the main entity to get.</span></span>

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

### <span data-ttu-id="82aa2-131">-Filter</span><span class="sxs-lookup"><span data-stu-id="82aa2-131">-Filter</span></span>
<span data-ttu-id="82aa2-132">Указывает предложение фильтра OData для задач.</span><span class="sxs-lookup"><span data-stu-id="82aa2-132">Specifies an OData filter clause for tasks.</span></span>
<span data-ttu-id="82aa2-133">Если не указать фильтр, этот cmdlet возвратит все задачи для учетной записи или задания пакета.</span><span class="sxs-lookup"><span data-stu-id="82aa2-133">If you do not specify a filter, this cmdlet returns all tasks for the Batch account or job.</span></span>

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

### <span data-ttu-id="82aa2-134">-Id</span><span class="sxs-lookup"><span data-stu-id="82aa2-134">-Id</span></span>
<span data-ttu-id="82aa2-135">Определяет код задачи, которая возвращается этим cmdletом.</span><span class="sxs-lookup"><span data-stu-id="82aa2-135">Specifies the ID of the task that this cmdlet gets.</span></span>
<span data-ttu-id="82aa2-136">Поддиавные знаки указывать нельзя.</span><span class="sxs-lookup"><span data-stu-id="82aa2-136">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82aa2-137">-Job</span><span class="sxs-lookup"><span data-stu-id="82aa2-137">-Job</span></span>
<span data-ttu-id="82aa2-138">Задание, которое содержит задачи, которые получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82aa2-138">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="82aa2-139">Чтобы получить объект **PSCloudJob,** используйте Get-AzBatchJob-код.</span><span class="sxs-lookup"><span data-stu-id="82aa2-139">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82aa2-140">-JobId</span><span class="sxs-lookup"><span data-stu-id="82aa2-140">-JobId</span></span>
<span data-ttu-id="82aa2-141">Определяет код задания, содержаща задачи, которые получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82aa2-141">Specifies the ID of the job that contains the tasks that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter, Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82aa2-142">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="82aa2-142">-MaxCount</span></span>
<span data-ttu-id="82aa2-143">Указывает максимальное количество возвращаемых задач.</span><span class="sxs-lookup"><span data-stu-id="82aa2-143">Specifies the maximum number of tasks to return.</span></span>
<span data-ttu-id="82aa2-144">Если указать нулевое (ноль) или меньшее значение, для cmdlet не используется верхний предел.</span><span class="sxs-lookup"><span data-stu-id="82aa2-144">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="82aa2-145">Значение по умолчанию — 1000.</span><span class="sxs-lookup"><span data-stu-id="82aa2-145">The default value is 1000.</span></span>

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

### <span data-ttu-id="82aa2-146">-Select</span><span class="sxs-lookup"><span data-stu-id="82aa2-146">-Select</span></span>
<span data-ttu-id="82aa2-147">Указывает предложение выбора OData.</span><span class="sxs-lookup"><span data-stu-id="82aa2-147">Specifies an OData select clause.</span></span>
<span data-ttu-id="82aa2-148">Укажите значение для этого параметра, чтобы получить определенные свойства, а не все свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="82aa2-148">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="82aa2-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82aa2-149">CommonParameters</span></span>
<span data-ttu-id="82aa2-150">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82aa2-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82aa2-151">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="82aa2-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82aa2-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="82aa2-152">INPUTS</span></span>

### <span data-ttu-id="82aa2-153">System.String</span><span class="sxs-lookup"><span data-stu-id="82aa2-153">System.String</span></span>

### <span data-ttu-id="82aa2-154">Microsoft.Azure.Commands.Batch. Models.PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="82aa2-154">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="82aa2-155">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="82aa2-155">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="82aa2-156">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="82aa2-156">OUTPUTS</span></span>

### <span data-ttu-id="82aa2-157">Microsoft.Azure.Commands.Batch. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="82aa2-157">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

## <span data-ttu-id="82aa2-158">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="82aa2-158">NOTES</span></span>

## <span data-ttu-id="82aa2-159">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="82aa2-159">RELATED LINKS</span></span>

[<span data-ttu-id="82aa2-160">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="82aa2-160">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="82aa2-161">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="82aa2-161">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="82aa2-162">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="82aa2-162">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="82aa2-163">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="82aa2-163">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="82aa2-164">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="82aa2-164">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="82aa2-165">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="82aa2-165">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
