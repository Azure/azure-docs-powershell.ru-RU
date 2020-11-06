---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 2B4BFDDA-9721-42E6-84E1-A209CB782954
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchTask.md
ms.openlocfilehash: dd8825be6491b0a0c8c8589f77180b38f9f230d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565653"
---
# <span data-ttu-id="ce8e1-101">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="ce8e1-101">New-AzureBatchTask</span></span>

## <span data-ttu-id="ce8e1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ce8e1-102">SYNOPSIS</span></span>
<span data-ttu-id="ce8e1-103">Создает пакетную задачу под заданием.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-103">Creates a Batch task under a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce8e1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ce8e1-104">SYNTAX</span></span>

### <span data-ttu-id="ce8e1-105">JobId_Single (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ce8e1-105">JobId_Single (Default)</span></span>
```
New-AzureBatchTask -JobId <String> -Id <String> [-DisplayName <String>] [-CommandLine <String>]
 [-ResourceFiles <IDictionary>] [-EnvironmentSettings <IDictionary>] [-RunElevated]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-ExitConditions <PSExitConditions>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce8e1-106">JobId_Bulk</span><span class="sxs-lookup"><span data-stu-id="ce8e1-106">JobId_Bulk</span></span>
```
New-AzureBatchTask -JobId <String> [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce8e1-107">JobObject_Bulk</span><span class="sxs-lookup"><span data-stu-id="ce8e1-107">JobObject_Bulk</span></span>
```
New-AzureBatchTask [-Job <PSCloudJob>] [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce8e1-108">JobObject_Single</span><span class="sxs-lookup"><span data-stu-id="ce8e1-108">JobObject_Single</span></span>
```
New-AzureBatchTask [-Job <PSCloudJob>] -Id <String> [-DisplayName <String>] [-CommandLine <String>]
 [-ResourceFiles <IDictionary>] [-EnvironmentSettings <IDictionary>] [-RunElevated]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-ExitConditions <PSExitConditions>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce8e1-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ce8e1-109">DESCRIPTION</span></span>
<span data-ttu-id="ce8e1-110">Командлет **New-AzureBatchTask** создает пакетную задачу Azure в задании, указанной параметром *JOBID* , или параметром *задания* .</span><span class="sxs-lookup"><span data-stu-id="ce8e1-110">The **New-AzureBatchTask** cmdlet creates an Azure Batch task under the job specified by the *JobId* parameter or the *Job* parameter.</span></span>

## <span data-ttu-id="ce8e1-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ce8e1-111">EXAMPLES</span></span>

### <span data-ttu-id="ce8e1-112">Пример 1: создание пакетной задачи</span><span class="sxs-lookup"><span data-stu-id="ce8e1-112">Example 1: Create a Batch task</span></span>
```
PS C:\>New-AzureBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
```

<span data-ttu-id="ce8e1-113">Эта команда создает задачу с ИДЕНТИФИКАТОРом Task23 под заданием с ИДЕНТИФИКАТОРом задания 000001.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-113">This command creates a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="ce8e1-114">Задача запускает указанную команду.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-114">The task runs the specified command.</span></span>
<span data-ttu-id="ce8e1-115">Используйте командлет **Get-AzureRmBatchAccountKeys** , чтобы назначить контекст переменной $context.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-115">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="ce8e1-116">Пример 2: создание пакетной задачи</span><span class="sxs-lookup"><span data-stu-id="ce8e1-116">Example 2: Create a Batch task</span></span>
```
PS C:\>Get-AzureBatchJob -Id "Job-000001" -BatchContext $Context | New-AzureBatchTask -Id "Task26" -CommandLine "cmd /c echo hello > newFile.txt" -RunElevated -BatchContext $Context
```

<span data-ttu-id="ce8e1-117">Эта команда получает пакетное задание с ИД задания, 000001 с помощью командлета **Get-AzureBatchJob** .</span><span class="sxs-lookup"><span data-stu-id="ce8e1-117">This command gets the Batch job that has the ID Job-000001 by using the **Get-AzureBatchJob** cmdlet.</span></span>
<span data-ttu-id="ce8e1-118">Команда передает это задание текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-118">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ce8e1-119">Команда создает задачу с ИДЕНТИФИКАТОРом Task26 под этим заданием.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-119">The command creates a task that has the ID Task26 under that job.</span></span>
<span data-ttu-id="ce8e1-120">Задача выполняет указанную команду с повышенными разрешениями.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-120">The task runs the specified command by using elevated permissions.</span></span>

### <span data-ttu-id="ce8e1-121">Пример 3: Добавление коллекции задач к указанному заданию с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="ce8e1-121">Example 3: Add a collection of tasks to the specified job by using the pipeline</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> Get-AzureBatchJob -Id "Job-000001" -BatchContext $Context | New-AzureBatchTask -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="ce8e1-122">Первая команда создает ссылку на объект для учетной записи пакетной службы с именем ContosoBatchAccount с помощью **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-122">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="ce8e1-123">Команда сохраняет ссылку на этот объект в переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-123">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="ce8e1-124">Следующие две команды создают объекты **PSCloudTask** с помощью командлета New-Object.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-124">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="ce8e1-125">Команды хранят задачи в $Task 01 и $Task 02.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-125">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>

<span data-ttu-id="ce8e1-126">Последняя команда получает пакетное задание с ИД задания 000001 с помощью **Get-AzureBatchJob**.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-126">The final command gets the Batch job that has the ID Job-000001 by using **Get-AzureBatchJob**.</span></span>
<span data-ttu-id="ce8e1-127">Затем команда передает это задание текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-127">Then the command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ce8e1-128">Команда добавляет коллекцию задач под этим заданием.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-128">The command adds a collection of tasks under that job.</span></span>
<span data-ttu-id="ce8e1-129">Команда использует контекст, хранящийся в $Context.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-129">The command uses the context stored in $Context.</span></span>

### <span data-ttu-id="ce8e1-130">Пример 4: Добавление коллекции задач к указанному заданию</span><span class="sxs-lookup"><span data-stu-id="ce8e1-130">Example 4: Add a collection of tasks to the specified job</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> New-AzureBatchTask -JobId "Job-000001" -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="ce8e1-131">Первая команда создает ссылку на объект для учетной записи пакетной службы с именем ContosoBatchAccount с помощью **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-131">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="ce8e1-132">Команда сохраняет ссылку на этот объект в переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-132">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="ce8e1-133">Следующие две команды создают объекты **PSCloudTask** с помощью командлета New-Object.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-133">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="ce8e1-134">Команды хранят задачи в $Task 01 и $Task 02.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-134">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>

<span data-ttu-id="ce8e1-135">Последняя команда добавляет задачи, которые хранятся в $Task 01 и $Task 02 под заданием с ИД задания 000001.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-135">The final command adds the tasks stored in $Task01 and $Task02 under the job that has the ID Job-000001.</span></span>

## <span data-ttu-id="ce8e1-136">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ce8e1-136">PARAMETERS</span></span>

### <span data-ttu-id="ce8e1-137">-AffinityInformation</span><span class="sxs-lookup"><span data-stu-id="ce8e1-137">-AffinityInformation</span></span>
<span data-ttu-id="ce8e1-138">Указывает подсказку о расположении, которую служба Batch использует для выбора узла, на котором необходимо выполнить задачу.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-138">Specifies a locality hint that the Batch service uses to select a node on which to run the task.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSAffinityInformation
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce8e1-139">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="ce8e1-139">-ApplicationPackageReferences</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSApplicationPackageReference[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce8e1-140">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ce8e1-140">-BatchContext</span></span>
<span data-ttu-id="ce8e1-141">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-141">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ce8e1-142">Чтобы получить объект **BatchAccountContext** , содержащий клавиши доступа для вашей подписки, используйте командлет Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-142">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="ce8e1-143">-CommandLine</span><span class="sxs-lookup"><span data-stu-id="ce8e1-143">-CommandLine</span></span>
<span data-ttu-id="ce8e1-144">Задает командную строку для задачи.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-144">Specifies the command line for the task.</span></span>

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce8e1-145">-Ограничения</span><span class="sxs-lookup"><span data-stu-id="ce8e1-145">-Constraints</span></span>
<span data-ttu-id="ce8e1-146">Указывает ограничения на выполнение, которые применяются к этой задаче.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-146">Specifies the execution constraints that apply to this task.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce8e1-147">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="ce8e1-147">-DependsOn</span></span>
<span data-ttu-id="ce8e1-148">Указывает, что задача зависит от других задач.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-148">Specifies that the task depends on other tasks.</span></span>
<span data-ttu-id="ce8e1-149">Задача не будет планироваться до тех пор, пока все зависимые задачи не будут выполнены успешно.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-149">The task will not be scheduled until all depended-on tasks have completed successfully.</span></span>

```yaml
Type: Microsoft.Azure.Batch.TaskDependencies
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce8e1-150">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ce8e1-150">-DisplayName</span></span>
<span data-ttu-id="ce8e1-151">Указывает отображаемое имя задачи.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-151">Specifies the display name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce8e1-152">-EnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="ce8e1-152">-EnvironmentSettings</span></span>
<span data-ttu-id="ce8e1-153">Задает параметры среды в виде пар "ключ-значение", которые этот командлет добавляет к задаче.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-153">Specifies the environment settings, as key/value pairs, that this cmdlet adds to the task.</span></span>
<span data-ttu-id="ce8e1-154">Ключом является имя параметра среды.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-154">The key is the environment setting name.</span></span>
<span data-ttu-id="ce8e1-155">Значение является параметром среды.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-155">The value is the environment setting.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce8e1-156">-ExitConditions</span><span class="sxs-lookup"><span data-stu-id="ce8e1-156">-ExitConditions</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSExitConditions
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce8e1-157">-ID</span><span class="sxs-lookup"><span data-stu-id="ce8e1-157">-Id</span></span>
<span data-ttu-id="ce8e1-158">Указывает идентификатор задачи.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-158">Specifies the ID of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce8e1-159">-Job</span><span class="sxs-lookup"><span data-stu-id="ce8e1-159">-Job</span></span>
<span data-ttu-id="ce8e1-160">Указывает задание, в рамках которого этот командлет создает задачу.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-160">Specifies the job under which this cmdlet creates the task.</span></span>
<span data-ttu-id="ce8e1-161">Чтобы получить объект **PSCloudJob** , используйте командлет Get-AzureBatchJob.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-161">To obtain a **PSCloudJob** object, use the Get-AzureBatchJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: JobObject_Bulk, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce8e1-162">-JobId</span><span class="sxs-lookup"><span data-stu-id="ce8e1-162">-JobId</span></span>
<span data-ttu-id="ce8e1-163">Указывает идентификатор задания, в рамках которого этот командлет создает задачу.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-163">Specifies the ID of the job under which this cmdlet creates the task.</span></span>

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobId_Bulk
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce8e1-164">-MultiInstanceSettings</span><span class="sxs-lookup"><span data-stu-id="ce8e1-164">-MultiInstanceSettings</span></span>
<span data-ttu-id="ce8e1-165">Задает сведения о том, как выполнить задачу с несколькими экземплярами.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-165">Specifies information about how to run a multi-instance task.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce8e1-166">-ResourceFiles</span><span class="sxs-lookup"><span data-stu-id="ce8e1-166">-ResourceFiles</span></span>
<span data-ttu-id="ce8e1-167">Определяет файлы ресурсов в виде пар "ключ-значение", которые требуются для задачи.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-167">Specifies resource files, as key/value pairs, that the task requires.</span></span>
<span data-ttu-id="ce8e1-168">Key — путь к файлу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-168">The key is the resource file path.</span></span>
<span data-ttu-id="ce8e1-169">Значением является источник больших двоичных объектов файла ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-169">The value is the resource file blob source.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce8e1-170">-RunElevated</span><span class="sxs-lookup"><span data-stu-id="ce8e1-170">-RunElevated</span></span>
<span data-ttu-id="ce8e1-171">Указывает на то, что рабочий процесс запускается с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-171">Indicates that the task process runs with administrator privileges.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce8e1-172">-Задачи</span><span class="sxs-lookup"><span data-stu-id="ce8e1-172">-Tasks</span></span>
<span data-ttu-id="ce8e1-173">Указывает коллекцию задач, которые нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-173">Specifies the collection of tasks to be added.</span></span>
<span data-ttu-id="ce8e1-174">Каждая задача должна иметь уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-174">Each task must have a unique ID.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask[]
Parameter Sets: JobId_Bulk, JobObject_Bulk
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce8e1-175">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce8e1-175">-DefaultProfile</span></span>
<span data-ttu-id="ce8e1-176">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-176">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce8e1-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce8e1-177">CommonParameters</span></span>
<span data-ttu-id="ce8e1-178">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce8e1-179">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce8e1-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce8e1-180">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ce8e1-180">INPUTS</span></span>

### <span data-ttu-id="ce8e1-181">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ce8e1-181">BatchAccountContext</span></span>
<span data-ttu-id="ce8e1-182">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-182">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="ce8e1-183">PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="ce8e1-183">PSCloudJob</span></span>
<span data-ttu-id="ce8e1-184">Параметр "задание" принимает значение типа "PSCloudJob" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="ce8e1-184">Parameter 'Job' accepts value of type 'PSCloudJob' from the pipeline</span></span>

## <span data-ttu-id="ce8e1-185">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ce8e1-185">OUTPUTS</span></span>

## <span data-ttu-id="ce8e1-186">Пуск</span><span class="sxs-lookup"><span data-stu-id="ce8e1-186">NOTES</span></span>

## <span data-ttu-id="ce8e1-187">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ce8e1-187">RELATED LINKS</span></span>

[<span data-ttu-id="ce8e1-188">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="ce8e1-188">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="ce8e1-189">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="ce8e1-189">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="ce8e1-190">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="ce8e1-190">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="ce8e1-191">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="ce8e1-191">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="ce8e1-192">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="ce8e1-192">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="ce8e1-193">Остановить-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="ce8e1-193">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="ce8e1-194">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="ce8e1-194">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


