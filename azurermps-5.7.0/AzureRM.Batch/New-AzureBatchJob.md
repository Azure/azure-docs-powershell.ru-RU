---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B6229D26-D38C-44CD-B9CA-7F39365C8B9D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJob.md
ms.openlocfilehash: bf96b5930895332de2e78ffdee71f9f6a2654b83
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570000"
---
# <span data-ttu-id="8bd40-101">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="8bd40-101">New-AzureBatchJob</span></span>

## <span data-ttu-id="8bd40-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8bd40-102">SYNOPSIS</span></span>
<span data-ttu-id="8bd40-103">Создание задания в пакетной службе.</span><span class="sxs-lookup"><span data-stu-id="8bd40-103">Creates a job in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8bd40-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8bd40-104">SYNTAX</span></span>

```
New-AzureBatchJob [-Id] <String> [-CommonEnvironmentSettings <IDictionary>] [-DisplayName <String>]
 [-Constraints <PSJobConstraints>] [-JobManagerTask <PSJobManagerTask>]
 [-JobPreparationTask <PSJobPreparationTask>] [-JobReleaseTask <PSJobReleaseTask>] [-Metadata <IDictionary>]
 -PoolInformation <PSPoolInformation> [-Priority <Int32>] [-UsesTaskDependencies]
 [-OnTaskFailure <OnTaskFailure>] [-OnAllTasksComplete <OnAllTasksComplete>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8bd40-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8bd40-105">DESCRIPTION</span></span>
<span data-ttu-id="8bd40-106">Командлет **New-AzureBatchJob** создает задание в пакетной службе Azure в учетной записи, указанной в параметре *BatchAccountContext* .</span><span class="sxs-lookup"><span data-stu-id="8bd40-106">The **New-AzureBatchJob** cmdlet creates a job in the Azure Batch service in the account specified by the *BatchAccountContext* parameter.</span></span>

## <span data-ttu-id="8bd40-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8bd40-107">EXAMPLES</span></span>

### <span data-ttu-id="8bd40-108">Пример 1: создание задания</span><span class="sxs-lookup"><span data-stu-id="8bd40-108">Example 1: Create a job</span></span>
```
PS C:\>$PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation" 
PS C:\> $PoolInformation.PoolId = "Pool22" 
PS C:\> New-AzureBatchJob -Id "ContosoJob35" -PoolInformation $PoolInformation -BatchContext $Context
```

<span data-ttu-id="8bd40-109">Первая команда создает объект **PSPoolInformation** с помощью командлета New-Object.</span><span class="sxs-lookup"><span data-stu-id="8bd40-109">The first command creates a **PSPoolInformation** object by using the New-Object cmdlet.</span></span>
<span data-ttu-id="8bd40-110">Команда сохраняет этот объект в переменной $PoolInformation.</span><span class="sxs-lookup"><span data-stu-id="8bd40-110">The command stores that object in the $PoolInformation variable.</span></span>

<span data-ttu-id="8bd40-111">Вторая команда присваивает идентификатор Pool22 свойству **PoolId** объекта в $PoolInformation.</span><span class="sxs-lookup"><span data-stu-id="8bd40-111">The second command assigns the ID Pool22 to the **PoolId** property of the object in $PoolInformation.</span></span>

<span data-ttu-id="8bd40-112">Последняя команда создает задание с ИДЕНТИФИКАТОРом ContosoJob35.</span><span class="sxs-lookup"><span data-stu-id="8bd40-112">The final command creates a job that has the ID ContosoJob35.</span></span>
<span data-ttu-id="8bd40-113">Задачи, добавленные в задание, выполняются в пуле с ИД Pool22.</span><span class="sxs-lookup"><span data-stu-id="8bd40-113">Tasks added to the job run on the pool that has the ID Pool22.</span></span>
<span data-ttu-id="8bd40-114">Используйте командлет Get-AzureRmBatchAccountKeys для присвоения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="8bd40-114">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="8bd40-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8bd40-115">PARAMETERS</span></span>

### <span data-ttu-id="8bd40-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="8bd40-116">-BatchContext</span></span>
<span data-ttu-id="8bd40-117">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="8bd40-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8bd40-118">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="8bd40-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="8bd40-119">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="8bd40-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="8bd40-120">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="8bd40-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="8bd40-121">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="8bd40-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8bd40-122">-CommonEnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="8bd40-122">-CommonEnvironmentSettings</span></span>
<span data-ttu-id="8bd40-123">Задает общие переменные среды, такие как пары "ключ-значение", которые устанавливаются этим командлетом для всех задач в задании.</span><span class="sxs-lookup"><span data-stu-id="8bd40-123">Specifies the common environment variables, as key/value pairs, that this cmdlet sets for all tasks in the job.</span></span>
<span data-ttu-id="8bd40-124">Ключом является имя переменной среды.</span><span class="sxs-lookup"><span data-stu-id="8bd40-124">The key is the environment variable name.</span></span>
<span data-ttu-id="8bd40-125">Значением является значение переменной среды.</span><span class="sxs-lookup"><span data-stu-id="8bd40-125">The value is the environment variable value.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: CommonEnvironmentSetting

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bd40-126">-Ограничения</span><span class="sxs-lookup"><span data-stu-id="8bd40-126">-Constraints</span></span>
<span data-ttu-id="8bd40-127">Указывает ограничения на выполнение для задания.</span><span class="sxs-lookup"><span data-stu-id="8bd40-127">Specifies the execution constraints for the job.</span></span>

```yaml
Type: PSJobConstraints
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bd40-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bd40-128">-DefaultProfile</span></span>
<span data-ttu-id="8bd40-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8bd40-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bd40-130">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8bd40-130">-DisplayName</span></span>
<span data-ttu-id="8bd40-131">Указывает отображаемое имя задания.</span><span class="sxs-lookup"><span data-stu-id="8bd40-131">Specifies the display name for the job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bd40-132">-ID</span><span class="sxs-lookup"><span data-stu-id="8bd40-132">-Id</span></span>
<span data-ttu-id="8bd40-133">Указывает идентификатор задания.</span><span class="sxs-lookup"><span data-stu-id="8bd40-133">Specifies an ID for the job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bd40-134">-JobManagerTask</span><span class="sxs-lookup"><span data-stu-id="8bd40-134">-JobManagerTask</span></span>
<span data-ttu-id="8bd40-135">Указывает задачу диспетчера задач.</span><span class="sxs-lookup"><span data-stu-id="8bd40-135">Specifies the Job Manager task.</span></span>
<span data-ttu-id="8bd40-136">Пакетная служба запускает задачу "Диспетчер задач" при запуске задания.</span><span class="sxs-lookup"><span data-stu-id="8bd40-136">The Batch service runs the Job Manager task when the job is started.</span></span>

```yaml
Type: PSJobManagerTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bd40-137">-JobPreparationTask</span><span class="sxs-lookup"><span data-stu-id="8bd40-137">-JobPreparationTask</span></span>
<span data-ttu-id="8bd40-138">Указывает задачу подготовки задания.</span><span class="sxs-lookup"><span data-stu-id="8bd40-138">Specifies the Job Preparation task.</span></span>
<span data-ttu-id="8bd40-139">Пакетная служба запускает задачу подготовки задания на вычислительном узле, прежде чем она начнет выполнение каких-либо задач этого задания на этом вычислительном узле.</span><span class="sxs-lookup"><span data-stu-id="8bd40-139">The Batch service runs the Job Preparation task on a compute node before it starts any tasks of that job on that compute node.</span></span>

```yaml
Type: PSJobPreparationTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bd40-140">-JobReleaseTask</span><span class="sxs-lookup"><span data-stu-id="8bd40-140">-JobReleaseTask</span></span>
<span data-ttu-id="8bd40-141">Указывает задачу выпуска задания.</span><span class="sxs-lookup"><span data-stu-id="8bd40-141">Specifies the Job Release task.</span></span>
<span data-ttu-id="8bd40-142">Пакетная служба запускает задачу задания выпуска, когда задание завершается.</span><span class="sxs-lookup"><span data-stu-id="8bd40-142">The Batch service runs the Job Release task when the job ends.</span></span>
<span data-ttu-id="8bd40-143">Пакетная служба запускает задачу выпуска задания на каждом из узлов вычислительной сети, в которых выполнялась какая-либо задача задания.</span><span class="sxs-lookup"><span data-stu-id="8bd40-143">The Batch service runs the Job Release task on each compute node where it ran any task of the job.</span></span>

```yaml
Type: PSJobReleaseTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bd40-144">-Metadata</span><span class="sxs-lookup"><span data-stu-id="8bd40-144">-Metadata</span></span>
<span data-ttu-id="8bd40-145">Задает метаданные в виде пар "ключ-значение", которые нужно добавить в задание.</span><span class="sxs-lookup"><span data-stu-id="8bd40-145">Specifies metadata, as key/value pairs, to add to the job.</span></span>
<span data-ttu-id="8bd40-146">Ключом является имя метаданных.</span><span class="sxs-lookup"><span data-stu-id="8bd40-146">The key is the metadata name.</span></span>
<span data-ttu-id="8bd40-147">Значением является значение метаданных.</span><span class="sxs-lookup"><span data-stu-id="8bd40-147">The value is the metadata value.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bd40-148">-OnAllTasksComplete</span><span class="sxs-lookup"><span data-stu-id="8bd40-148">-OnAllTasksComplete</span></span>
<span data-ttu-id="8bd40-149">Указывает действие, выполняемое пакетной службой, если все задачи в задании находятся в завершенном состоянии.</span><span class="sxs-lookup"><span data-stu-id="8bd40-149">Specifies an action the Batch service takes if all tasks in the job are in the completed state.</span></span>

```yaml
Type: OnAllTasksComplete
Parameter Sets: (All)
Aliases: 
Accepted values: NoAction, TerminateJob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bd40-150">-OnTaskFailure</span><span class="sxs-lookup"><span data-stu-id="8bd40-150">-OnTaskFailure</span></span>
<span data-ttu-id="8bd40-151">Указывает действие, выполняемое пакетной службой в случае сбоя какой – либо задачи в задании.</span><span class="sxs-lookup"><span data-stu-id="8bd40-151">Specifies an action the Batch service takes if any task in the job fails.</span></span>

```yaml
Type: OnTaskFailure
Parameter Sets: (All)
Aliases: 
Accepted values: NoAction, PerformExitOptionsJobAction

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bd40-152">-PoolInformation</span><span class="sxs-lookup"><span data-stu-id="8bd40-152">-PoolInformation</span></span>
<span data-ttu-id="8bd40-153">Задает сведения о пуле, в котором Пакетная служба выполняет задачи задания.</span><span class="sxs-lookup"><span data-stu-id="8bd40-153">Specifies the details of the pool on which the Batch service runs the tasks of the job.</span></span>

```yaml
Type: PSPoolInformation
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bd40-154">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="8bd40-154">-Priority</span></span>
<span data-ttu-id="8bd40-155">Задает приоритет задания.</span><span class="sxs-lookup"><span data-stu-id="8bd40-155">Specifies the priority of the job.</span></span>
<span data-ttu-id="8bd40-156">Допустимые значения: целые числа от-1000 до 1000.</span><span class="sxs-lookup"><span data-stu-id="8bd40-156">Valid values are: integers from -1000 to 1000.</span></span>
<span data-ttu-id="8bd40-157">Значение-1000 является самым низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="8bd40-157">A value of -1000 is the lowest priority.</span></span>
<span data-ttu-id="8bd40-158">Значение 1000 — самый высокий приоритет.</span><span class="sxs-lookup"><span data-stu-id="8bd40-158">A value of 1000 is the highest priority.</span></span>
<span data-ttu-id="8bd40-159">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="8bd40-159">The default value is 0.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bd40-160">-UsesTaskDependencies</span><span class="sxs-lookup"><span data-stu-id="8bd40-160">-UsesTaskDependencies</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bd40-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bd40-161">CommonParameters</span></span>
<span data-ttu-id="8bd40-162">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8bd40-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bd40-163">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bd40-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bd40-164">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8bd40-164">INPUTS</span></span>

### <span data-ttu-id="8bd40-165">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8bd40-165">BatchAccountContext</span></span>
<span data-ttu-id="8bd40-166">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="8bd40-166">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="8bd40-167">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8bd40-167">OUTPUTS</span></span>

## <span data-ttu-id="8bd40-168">Пуск</span><span class="sxs-lookup"><span data-stu-id="8bd40-168">NOTES</span></span>

## <span data-ttu-id="8bd40-169">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8bd40-169">RELATED LINKS</span></span>

[<span data-ttu-id="8bd40-170">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="8bd40-170">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="8bd40-171">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="8bd40-171">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="8bd40-172">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="8bd40-172">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="8bd40-173">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="8bd40-173">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="8bd40-174">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="8bd40-174">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="8bd40-175">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="8bd40-175">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="8bd40-176">Остановить-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="8bd40-176">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="8bd40-177">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="8bd40-177">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


