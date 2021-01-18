---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B6229D26-D38C-44CD-B9CA-7F39365C8B9D
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJob.md
ms.openlocfilehash: f997c1574a81badf9d97bb4afecc104990aa725b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509638"
---
# <span data-ttu-id="401f9-101">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="401f9-101">New-AzBatchJob</span></span>

## <span data-ttu-id="401f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="401f9-102">SYNOPSIS</span></span>
<span data-ttu-id="401f9-103">Создает задание в службе обработки пакетов.</span><span class="sxs-lookup"><span data-stu-id="401f9-103">Creates a job in the Batch service.</span></span>

## <span data-ttu-id="401f9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="401f9-104">SYNTAX</span></span>

```
New-AzBatchJob [-Id] <String> [-CommonEnvironmentSettings <IDictionary>] [-DisplayName <String>]
 [-Constraints <PSJobConstraints>] [-JobManagerTask <PSJobManagerTask>]
 [-JobPreparationTask <PSJobPreparationTask>] [-JobReleaseTask <PSJobReleaseTask>] [-Metadata <IDictionary>]
 -PoolInformation <PSPoolInformation> [-Priority <Int32>] [-UsesTaskDependencies]
 [-OnTaskFailure <OnTaskFailure>] [-OnAllTasksComplete <OnAllTasksComplete>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="401f9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="401f9-105">DESCRIPTION</span></span>
<span data-ttu-id="401f9-106">Для создания задания в службе Azure Batch в учетной записи, задаваемой параметром *BatchAccountContext,* создается задание **new-AzBatchJob.**</span><span class="sxs-lookup"><span data-stu-id="401f9-106">The **New-AzBatchJob** cmdlet creates a job in the Azure Batch service in the account specified by the *BatchAccountContext* parameter.</span></span>

## <span data-ttu-id="401f9-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="401f9-107">EXAMPLES</span></span>

### <span data-ttu-id="401f9-108">Пример 1. Создание задания</span><span class="sxs-lookup"><span data-stu-id="401f9-108">Example 1: Create a job</span></span>
```
PS C:\>$PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation"
PS C:\> $PoolInformation.PoolId = "Pool22"
PS C:\> New-AzBatchJob -Id "ContosoJob35" -PoolInformation $PoolInformation -BatchContext $Context
```

<span data-ttu-id="401f9-109">Первая команда создает объект **PSPoolInformation** с помощью New-Object командлета.</span><span class="sxs-lookup"><span data-stu-id="401f9-109">The first command creates a **PSPoolInformation** object by using the New-Object cmdlet.</span></span>
<span data-ttu-id="401f9-110">Эта команда сохраняет этот объект в переменной $PoolInformation.</span><span class="sxs-lookup"><span data-stu-id="401f9-110">The command stores that object in the $PoolInformation variable.</span></span>
<span data-ttu-id="401f9-111">Вторая команда назначает ID Pool22 свойству **PoolId** объекта в $PoolInformation.</span><span class="sxs-lookup"><span data-stu-id="401f9-111">The second command assigns the ID Pool22 to the **PoolId** property of the object in $PoolInformation.</span></span>
<span data-ttu-id="401f9-112">Конечная команда создает задание с ИД ContosoJob35.</span><span class="sxs-lookup"><span data-stu-id="401f9-112">The final command creates a job that has the ID ContosoJob35.</span></span>
<span data-ttu-id="401f9-113">Задачи, добавленные в задание, запускаются в пуле с пулом ID Pool22.</span><span class="sxs-lookup"><span data-stu-id="401f9-113">Tasks added to the job run on the pool that has the ID Pool22.</span></span>
<span data-ttu-id="401f9-114">Используйте Get-AzBatchAccountKey для назначения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="401f9-114">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="401f9-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="401f9-115">PARAMETERS</span></span>

### <span data-ttu-id="401f9-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="401f9-116">-BatchContext</span></span>
<span data-ttu-id="401f9-117">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="401f9-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="401f9-118">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой пакета будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="401f9-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="401f9-119">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="401f9-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="401f9-120">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="401f9-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="401f9-121">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="401f9-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="401f9-122">-CommonEnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="401f9-122">-CommonEnvironmentSettings</span></span>
<span data-ttu-id="401f9-123">Задает общие переменные среды, как пары ключей и значений, которые этот cmdlet задает для всех задач задания.</span><span class="sxs-lookup"><span data-stu-id="401f9-123">Specifies the common environment variables, as key/value pairs, that this cmdlet sets for all tasks in the job.</span></span>
<span data-ttu-id="401f9-124">Ключом является имя переменной среды.</span><span class="sxs-lookup"><span data-stu-id="401f9-124">The key is the environment variable name.</span></span>
<span data-ttu-id="401f9-125">Значение — это значение переменной среды.</span><span class="sxs-lookup"><span data-stu-id="401f9-125">The value is the environment variable value.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: CommonEnvironmentSetting

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="401f9-126">-Ограничения</span><span class="sxs-lookup"><span data-stu-id="401f9-126">-Constraints</span></span>
<span data-ttu-id="401f9-127">Определяет ограничения выполнения для задания.</span><span class="sxs-lookup"><span data-stu-id="401f9-127">Specifies the execution constraints for the job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobConstraints
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="401f9-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="401f9-128">-DefaultProfile</span></span>
<span data-ttu-id="401f9-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="401f9-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="401f9-130">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="401f9-130">-DisplayName</span></span>
<span data-ttu-id="401f9-131">Отображает имя задания.</span><span class="sxs-lookup"><span data-stu-id="401f9-131">Specifies the display name for the job.</span></span>

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

### <span data-ttu-id="401f9-132">-Id</span><span class="sxs-lookup"><span data-stu-id="401f9-132">-Id</span></span>
<span data-ttu-id="401f9-133">Определяет ИД задания.</span><span class="sxs-lookup"><span data-stu-id="401f9-133">Specifies an ID for the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="401f9-134">-JobManagerTask</span><span class="sxs-lookup"><span data-stu-id="401f9-134">-JobManagerTask</span></span>
<span data-ttu-id="401f9-135">Определяет задачу диспетчера вакансий.</span><span class="sxs-lookup"><span data-stu-id="401f9-135">Specifies the Job Manager task.</span></span>
<span data-ttu-id="401f9-136">Пакетная служба выполняет задачу "Диспетчер вакансий" при запуске задания.</span><span class="sxs-lookup"><span data-stu-id="401f9-136">The Batch service runs the Job Manager task when the job is started.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobManagerTask
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="401f9-137">-JobPreparationTask</span><span class="sxs-lookup"><span data-stu-id="401f9-137">-JobPreparationTask</span></span>
<span data-ttu-id="401f9-138">Указывает задачу по подготовке задания.</span><span class="sxs-lookup"><span data-stu-id="401f9-138">Specifies the Job Preparation task.</span></span>
<span data-ttu-id="401f9-139">Пакетная служба выполняет задачу "Подготовка задания" на узле компьютеров перед выполнением любых задач этого задания на этом узле.</span><span class="sxs-lookup"><span data-stu-id="401f9-139">The Batch service runs the Job Preparation task on a compute node before it starts any tasks of that job on that compute node.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTask
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="401f9-140">-JobReleaseTask</span><span class="sxs-lookup"><span data-stu-id="401f9-140">-JobReleaseTask</span></span>
<span data-ttu-id="401f9-141">Указывает задачу "Выпуск задания".</span><span class="sxs-lookup"><span data-stu-id="401f9-141">Specifies the Job Release task.</span></span>
<span data-ttu-id="401f9-142">Пакетная служба выполняет задачу "Выпуск задания" после ее окончания.</span><span class="sxs-lookup"><span data-stu-id="401f9-142">The Batch service runs the Job Release task when the job ends.</span></span>
<span data-ttu-id="401f9-143">Пакетная служба выполняет задачу "Выпуск задания" на каждом узле компьютеров, где она выполняет задачу задания.</span><span class="sxs-lookup"><span data-stu-id="401f9-143">The Batch service runs the Job Release task on each compute node where it ran any task of the job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobReleaseTask
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="401f9-144">-Метаданные</span><span class="sxs-lookup"><span data-stu-id="401f9-144">-Metadata</span></span>
<span data-ttu-id="401f9-145">Метаданные в качестве пар ключа и значения, которые нужно добавить в задание.</span><span class="sxs-lookup"><span data-stu-id="401f9-145">Specifies metadata, as key/value pairs, to add to the job.</span></span>
<span data-ttu-id="401f9-146">Ключ — это имя метаданных.</span><span class="sxs-lookup"><span data-stu-id="401f9-146">The key is the metadata name.</span></span>
<span data-ttu-id="401f9-147">Значение — это значение метаданных.</span><span class="sxs-lookup"><span data-stu-id="401f9-147">The value is the metadata value.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="401f9-148">-OnAllTasksComplete</span><span class="sxs-lookup"><span data-stu-id="401f9-148">-OnAllTasksComplete</span></span>
<span data-ttu-id="401f9-149">Указывает действие, выполненное службой обработки пакетов, если все задачи в задании находятся в завершеном состоянии.</span><span class="sxs-lookup"><span data-stu-id="401f9-149">Specifies an action the Batch service takes if all tasks in the job are in the completed state.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.OnAllTasksComplete]
Parameter Sets: (All)
Aliases:
Accepted values: NoAction, TerminateJob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="401f9-150">-OnTaskFailure</span><span class="sxs-lookup"><span data-stu-id="401f9-150">-OnTaskFailure</span></span>
<span data-ttu-id="401f9-151">Указывает действие, которую служба обработки пакетов принимает в случае сбой какой-либо задачи в задаче.</span><span class="sxs-lookup"><span data-stu-id="401f9-151">Specifies an action the Batch service takes if any task in the job fails.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.OnTaskFailure]
Parameter Sets: (All)
Aliases:
Accepted values: NoAction, PerformExitOptionsJobAction

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="401f9-152">-PoolInformation</span><span class="sxs-lookup"><span data-stu-id="401f9-152">-PoolInformation</span></span>
<span data-ttu-id="401f9-153">Определяет сведения о пуле, в котором выполняется задача задания в пакетной службе.</span><span class="sxs-lookup"><span data-stu-id="401f9-153">Specifies the details of the pool on which the Batch service runs the tasks of the job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="401f9-154">-Priority</span><span class="sxs-lookup"><span data-stu-id="401f9-154">-Priority</span></span>
<span data-ttu-id="401f9-155">Определяет приоритет задания.</span><span class="sxs-lookup"><span data-stu-id="401f9-155">Specifies the priority of the job.</span></span>
<span data-ttu-id="401f9-156">Допустимые значения: от -1000 до 1000.</span><span class="sxs-lookup"><span data-stu-id="401f9-156">Valid values are: integers from -1000 to 1000.</span></span>
<span data-ttu-id="401f9-157">Значение -1000 — это наименьший приоритет.</span><span class="sxs-lookup"><span data-stu-id="401f9-157">A value of -1000 is the lowest priority.</span></span>
<span data-ttu-id="401f9-158">1000 — это наивысший приоритет.</span><span class="sxs-lookup"><span data-stu-id="401f9-158">A value of 1000 is the highest priority.</span></span>
<span data-ttu-id="401f9-159">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="401f9-159">The default value is 0.</span></span>

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

### <span data-ttu-id="401f9-160">-UsesTaskDependencies</span><span class="sxs-lookup"><span data-stu-id="401f9-160">-UsesTaskDependencies</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="401f9-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="401f9-161">CommonParameters</span></span>
<span data-ttu-id="401f9-162">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="401f9-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="401f9-163">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="401f9-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="401f9-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="401f9-164">INPUTS</span></span>

### <span data-ttu-id="401f9-165">System.String</span><span class="sxs-lookup"><span data-stu-id="401f9-165">System.String</span></span>

### <span data-ttu-id="401f9-166">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="401f9-166">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="401f9-167">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="401f9-167">OUTPUTS</span></span>

### <span data-ttu-id="401f9-168">System.Void</span><span class="sxs-lookup"><span data-stu-id="401f9-168">System.Void</span></span>

## <span data-ttu-id="401f9-169">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="401f9-169">NOTES</span></span>

## <span data-ttu-id="401f9-170">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="401f9-170">RELATED LINKS</span></span>

[<span data-ttu-id="401f9-171">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="401f9-171">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="401f9-172">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="401f9-172">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="401f9-173">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="401f9-173">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="401f9-174">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="401f9-174">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="401f9-175">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="401f9-175">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="401f9-176">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="401f9-176">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="401f9-177">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="401f9-177">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="401f9-178">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="401f9-178">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
