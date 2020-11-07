---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2B4BFDDA-9721-42E6-84E1-A209CB782954
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchTask.md
ms.openlocfilehash: adb3a44a5d913d636d216750358ebd96c8fc5a29
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93731849"
---
# <span data-ttu-id="94e63-101">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="94e63-101">New-AzBatchTask</span></span>

## <span data-ttu-id="94e63-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="94e63-102">SYNOPSIS</span></span>
<span data-ttu-id="94e63-103">Создает пакетную задачу под заданием.</span><span class="sxs-lookup"><span data-stu-id="94e63-103">Creates a Batch task under a job.</span></span>

## <span data-ttu-id="94e63-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="94e63-104">SYNTAX</span></span>

### <span data-ttu-id="94e63-105">JobId_Single (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="94e63-105">JobId_Single (Default)</span></span>
```
New-AzBatchTask -JobId <String> -Id <String> [-DisplayName <String>] [-CommandLine <String>]
 [-ResourceFiles <IDictionary>] [-EnvironmentSettings <IDictionary>]
 [-AuthenticationTokenSettings <PSAuthenticationTokenSettings>] [-UserIdentity <PSUserIdentity>]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-OutputFile <PSOutputFile[]>]
 [-ExitConditions <PSExitConditions>] [-ContainerSettings <PSTaskContainerSettings>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94e63-106">JobId_Bulk</span><span class="sxs-lookup"><span data-stu-id="94e63-106">JobId_Bulk</span></span>
```
New-AzBatchTask -JobId <String> [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94e63-107">JobObject_Bulk</span><span class="sxs-lookup"><span data-stu-id="94e63-107">JobObject_Bulk</span></span>
```
New-AzBatchTask [-Job <PSCloudJob>] [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94e63-108">JobObject_Single</span><span class="sxs-lookup"><span data-stu-id="94e63-108">JobObject_Single</span></span>
```
New-AzBatchTask [-Job <PSCloudJob>] -Id <String> [-DisplayName <String>] [-CommandLine <String>]
 [-ResourceFiles <IDictionary>] [-EnvironmentSettings <IDictionary>]
 [-AuthenticationTokenSettings <PSAuthenticationTokenSettings>] [-UserIdentity <PSUserIdentity>]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-OutputFile <PSOutputFile[]>]
 [-ExitConditions <PSExitConditions>] [-ContainerSettings <PSTaskContainerSettings>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94e63-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="94e63-109">DESCRIPTION</span></span>
<span data-ttu-id="94e63-110">Командлет **New-AzBatchTask** создает пакетную задачу Azure в задании, указанной параметром *JOBID* , или параметром *задания* .</span><span class="sxs-lookup"><span data-stu-id="94e63-110">The **New-AzBatchTask** cmdlet creates an Azure Batch task under the job specified by the *JobId* parameter or the *Job* parameter.</span></span>

## <span data-ttu-id="94e63-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="94e63-111">EXAMPLES</span></span>

### <span data-ttu-id="94e63-112">Пример 1: создание пакетной задачи</span><span class="sxs-lookup"><span data-stu-id="94e63-112">Example 1: Create a Batch task</span></span>
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
```

<span data-ttu-id="94e63-113">Эта команда создает задачу с ИДЕНТИФИКАТОРом Task23 под заданием с ИДЕНТИФИКАТОРом задания 000001.</span><span class="sxs-lookup"><span data-stu-id="94e63-113">This command creates a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="94e63-114">Задача запускает указанную команду.</span><span class="sxs-lookup"><span data-stu-id="94e63-114">The task runs the specified command.</span></span>
<span data-ttu-id="94e63-115">Используйте командлет **Get-AzBatchAccountKeys** , чтобы назначить контекст переменной $context.</span><span class="sxs-lookup"><span data-stu-id="94e63-115">Use the **Get-AzBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="94e63-116">Пример 2: создание пакетной задачи</span><span class="sxs-lookup"><span data-stu-id="94e63-116">Example 2: Create a Batch task</span></span>
```
PS C:\> $autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
PS C:\> $userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
PS C:\>Get-AzBatchJob -Id "Job-000001" -BatchContext $Context | New-AzBatchTask -Id "Task26" -CommandLine "cmd /c echo hello > newFile.txt" -UserIdentity $userIdentity -BatchContext $Context
```

<span data-ttu-id="94e63-117">Эта команда получает пакетное задание с ИД задания, 000001 с помощью командлета **Get-AzBatchJob** .</span><span class="sxs-lookup"><span data-stu-id="94e63-117">This command gets the Batch job that has the ID Job-000001 by using the **Get-AzBatchJob** cmdlet.</span></span>
<span data-ttu-id="94e63-118">Команда передает это задание текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="94e63-118">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="94e63-119">Команда создает задачу с ИДЕНТИФИКАТОРом Task26 под этим заданием.</span><span class="sxs-lookup"><span data-stu-id="94e63-119">The command creates a task that has the ID Task26 under that job.</span></span>
<span data-ttu-id="94e63-120">Задача выполняет указанную команду с повышенными разрешениями.</span><span class="sxs-lookup"><span data-stu-id="94e63-120">The task runs the specified command by using elevated permissions.</span></span>

### <span data-ttu-id="94e63-121">Пример 3: Добавление коллекции задач к указанному заданию с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="94e63-121">Example 3: Add a collection of tasks to the specified job by using the pipeline</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> Get-AzBatchJob -Id "Job-000001" -BatchContext $Context | New-AzBatchTask -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="94e63-122">Первая команда создает ссылку на объект для учетной записи пакетной службы с именем ContosoBatchAccount с помощью **Get-AzBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="94e63-122">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKeys**.</span></span>
<span data-ttu-id="94e63-123">Команда сохраняет ссылку на этот объект в переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="94e63-123">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="94e63-124">Следующие две команды создают объекты **PSCloudTask** с помощью командлета New-Object.</span><span class="sxs-lookup"><span data-stu-id="94e63-124">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="94e63-125">Команды хранят задачи в $Task 01 и $Task 02.</span><span class="sxs-lookup"><span data-stu-id="94e63-125">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>
<span data-ttu-id="94e63-126">Последняя команда получает пакетное задание с ИД задания 000001 с помощью **Get-AzBatchJob**.</span><span class="sxs-lookup"><span data-stu-id="94e63-126">The final command gets the Batch job that has the ID Job-000001 by using **Get-AzBatchJob**.</span></span>
<span data-ttu-id="94e63-127">Затем команда передает это задание текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="94e63-127">Then the command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="94e63-128">Команда добавляет коллекцию задач под этим заданием.</span><span class="sxs-lookup"><span data-stu-id="94e63-128">The command adds a collection of tasks under that job.</span></span>
<span data-ttu-id="94e63-129">Команда использует контекст, хранящийся в $Context.</span><span class="sxs-lookup"><span data-stu-id="94e63-129">The command uses the context stored in $Context.</span></span>

### <span data-ttu-id="94e63-130">Пример 4: Добавление коллекции задач к указанному заданию</span><span class="sxs-lookup"><span data-stu-id="94e63-130">Example 4: Add a collection of tasks to the specified job</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> New-AzBatchTask -JobId "Job-000001" -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="94e63-131">Первая команда создает ссылку на объект для учетной записи пакетной службы с именем ContosoBatchAccount с помощью **Get-AzBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="94e63-131">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKeys**.</span></span>
<span data-ttu-id="94e63-132">Команда сохраняет ссылку на этот объект в переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="94e63-132">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="94e63-133">Следующие две команды создают объекты **PSCloudTask** с помощью командлета New-Object.</span><span class="sxs-lookup"><span data-stu-id="94e63-133">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="94e63-134">Команды хранят задачи в $Task 01 и $Task 02.</span><span class="sxs-lookup"><span data-stu-id="94e63-134">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>
<span data-ttu-id="94e63-135">Последняя команда добавляет задачи, которые хранятся в $Task 01 и $Task 02 под заданием с ИД задания 000001.</span><span class="sxs-lookup"><span data-stu-id="94e63-135">The final command adds the tasks stored in $Task01 and $Task02 under the job that has the ID Job-000001.</span></span>

### <span data-ttu-id="94e63-136">Пример 5: Добавление задачи с помощью выходных файлов</span><span class="sxs-lookup"><span data-stu-id="94e63-136">Example 5: Add a task with output files</span></span>
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
PS C:\>$blobContainerDestination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileBlobContainerDestination "https://myaccount.blob.core.windows.net/sascontainer?sv=2015-04-05&st=2015-04-29T22%3A18%3A26Z&se=2015-04-30T02%3A23%3A26Z&sr=b&sp=rw&spr=https&sig=Z%2FRHIX5Xcg0Mq2rqI3OlWTjEg2tYkboXr1P9ZUXDtkk%3D"
PS C:\>$destination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileDestination $blobContainerDestination
PS C:\>$uploadOptions = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileUploadOptions "TaskSuccess"
PS C:\>$outputFile = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFile "*.txt", $blobContainerDestination, $uploadOptions

PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -OutputFile $outputFile -BatchContext $Context
```

### <span data-ttu-id="94e63-137">Пример 6: Добавление задачи с помощью параметров маркеров проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="94e63-137">Example 6: Add a task with authentication token settings</span></span>
```
PS C:\>$authSettings = New-Object Microsoft.Azure.Commands.Batch.Models.PSAuthenticationTokenSettings
PS C:\>$authSettings.Access = "Job"
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -AuthenticationTokenSettings $authSettings -BatchContext $Context
```

### <span data-ttu-id="94e63-138">Пример 7: Добавление задачи, выполняемой в контейнере</span><span class="sxs-lookup"><span data-stu-id="94e63-138">Example 7: Add a task which runs in a container</span></span>
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ContainerSettings New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskContainerSettings "containerImageName"
```

## <span data-ttu-id="94e63-139">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="94e63-139">PARAMETERS</span></span>

### <span data-ttu-id="94e63-140">-AffinityInformation</span><span class="sxs-lookup"><span data-stu-id="94e63-140">-AffinityInformation</span></span>
<span data-ttu-id="94e63-141">Указывает подсказку о расположении, которую служба Batch использует для выбора узла, на котором необходимо выполнить задачу.</span><span class="sxs-lookup"><span data-stu-id="94e63-141">Specifies a locality hint that the Batch service uses to select a node on which to run the task.</span></span>

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

### <span data-ttu-id="94e63-142">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="94e63-142">-ApplicationPackageReferences</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSApplicationPackageReference[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases: ApplicationPackageReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94e63-143">-AuthenticationTokenSettings</span><span class="sxs-lookup"><span data-stu-id="94e63-143">-AuthenticationTokenSettings</span></span>
<span data-ttu-id="94e63-144">Параметры маркера проверки подлинности, который задача может использовать для выполнения операций пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="94e63-144">The settings for an authentication token that the task can use to perform Batch service operations.</span></span>
<span data-ttu-id="94e63-145">Если этот параметр задан, пакетная служба предоставляет задачу с маркером проверки подлинности, который можно использовать для проверки подлинности операций пакетной службы, не требуя ключа доступа учетной записи.</span><span class="sxs-lookup"><span data-stu-id="94e63-145">If this is set, the Batch service provides the task with an authentication token which can be used to authenticate Batch service operations without requiring an account access key.</span></span> <span data-ttu-id="94e63-146">Маркер предоставляется с помощью переменной среды AZ_BATCH_AUTHENTICATION_TOKEN.</span><span class="sxs-lookup"><span data-stu-id="94e63-146">The token is provided via the AZ_BATCH_AUTHENTICATION_TOKEN environment variable.</span></span> <span data-ttu-id="94e63-147">Операции, которые может выполнять задача с помощью маркера, зависят от параметров.</span><span class="sxs-lookup"><span data-stu-id="94e63-147">The operations that the task can carry out using the token depend on the settings.</span></span> <span data-ttu-id="94e63-148">Например, задача может запрашивать разрешения задания, чтобы добавить в задание другие задачи, или проверить состояние задания или других задач.</span><span class="sxs-lookup"><span data-stu-id="94e63-148">For example, a task can request job permissions in order to add other tasks to the job, or check the status of the job or of other tasks.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSAuthenticationTokenSettings
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94e63-149">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="94e63-149">-BatchContext</span></span>
<span data-ttu-id="94e63-150">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="94e63-150">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="94e63-151">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="94e63-151">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="94e63-152">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="94e63-152">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="94e63-153">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="94e63-153">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="94e63-154">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="94e63-154">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="94e63-155">-CommandLine</span><span class="sxs-lookup"><span data-stu-id="94e63-155">-CommandLine</span></span>
<span data-ttu-id="94e63-156">Задает командную строку для задачи.</span><span class="sxs-lookup"><span data-stu-id="94e63-156">Specifies the command line for the task.</span></span>

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

### <span data-ttu-id="94e63-157">-Ограничения</span><span class="sxs-lookup"><span data-stu-id="94e63-157">-Constraints</span></span>
<span data-ttu-id="94e63-158">Указывает ограничения на выполнение, которые применяются к этой задаче.</span><span class="sxs-lookup"><span data-stu-id="94e63-158">Specifies the execution constraints that apply to this task.</span></span>

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

### <span data-ttu-id="94e63-159">-ContainerSettings</span><span class="sxs-lookup"><span data-stu-id="94e63-159">-ContainerSettings</span></span>
<span data-ttu-id="94e63-160">Параметры для контейнера, в котором выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="94e63-160">The settings for the container under which the task runs.</span></span>
<span data-ttu-id="94e63-161">Если для пула, на котором будет выполняться эта задача, задано значение containerConfiguration, оно также должно быть задано.</span><span class="sxs-lookup"><span data-stu-id="94e63-161">If the pool that will run this task has containerConfiguration set, this must be set as well.</span></span> <span data-ttu-id="94e63-162">Если для пула, на котором будет выполняться эта задача, не задан containerConfiguration, этот параметр не должен быть установлен.</span><span class="sxs-lookup"><span data-stu-id="94e63-162">If the pool that will run this task doesn't have containerConfiguration set, this must not be set.</span></span> <span data-ttu-id="94e63-163">Если задано значение, все каталоги, рекурсивно расположенные под AZ_BATCH_NODE_ROOT_DIR (корень пакетных папок Azure на узле), сопоставляются с контейнером, все переменные среды задач сопоставляются с контейнером, а Командная строка задачи выполняется в контейнере.</span><span class="sxs-lookup"><span data-stu-id="94e63-163">When this is specified, all directories recursively below the AZ_BATCH_NODE_ROOT_DIR (the root of Azure Batch directories on the node) are mapped into the container, all task environment variables are mapped into the container, and the task command line is executed in the container.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSTaskContainerSettings
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94e63-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94e63-164">-DefaultProfile</span></span>
<span data-ttu-id="94e63-165">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="94e63-165">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94e63-166">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="94e63-166">-DependsOn</span></span>
<span data-ttu-id="94e63-167">Указывает, что задача зависит от других задач.</span><span class="sxs-lookup"><span data-stu-id="94e63-167">Specifies that the task depends on other tasks.</span></span>
<span data-ttu-id="94e63-168">Задача не будет планироваться до тех пор, пока все зависимые задачи не будут выполнены успешно.</span><span class="sxs-lookup"><span data-stu-id="94e63-168">The task will not be scheduled until all depended-on tasks have completed successfully.</span></span>

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

### <span data-ttu-id="94e63-169">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="94e63-169">-DisplayName</span></span>
<span data-ttu-id="94e63-170">Указывает отображаемое имя задачи.</span><span class="sxs-lookup"><span data-stu-id="94e63-170">Specifies the display name of the task.</span></span>

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

### <span data-ttu-id="94e63-171">-EnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="94e63-171">-EnvironmentSettings</span></span>
<span data-ttu-id="94e63-172">Задает параметры среды в виде пар "ключ-значение", которые этот командлет добавляет к задаче.</span><span class="sxs-lookup"><span data-stu-id="94e63-172">Specifies the environment settings, as key/value pairs, that this cmdlet adds to the task.</span></span>
<span data-ttu-id="94e63-173">Ключом является имя параметра среды.</span><span class="sxs-lookup"><span data-stu-id="94e63-173">The key is the environment setting name.</span></span>
<span data-ttu-id="94e63-174">Значение является параметром среды.</span><span class="sxs-lookup"><span data-stu-id="94e63-174">The value is the environment setting.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: JobId_Single, JobObject_Single
Aliases: EnvironmentSetting

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94e63-175">-ExitConditions</span><span class="sxs-lookup"><span data-stu-id="94e63-175">-ExitConditions</span></span>
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

### <span data-ttu-id="94e63-176">-ID</span><span class="sxs-lookup"><span data-stu-id="94e63-176">-Id</span></span>
<span data-ttu-id="94e63-177">Указывает идентификатор задачи.</span><span class="sxs-lookup"><span data-stu-id="94e63-177">Specifies the ID of the task.</span></span>

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

### <span data-ttu-id="94e63-178">-Job</span><span class="sxs-lookup"><span data-stu-id="94e63-178">-Job</span></span>
<span data-ttu-id="94e63-179">Указывает задание, в рамках которого этот командлет создает задачу.</span><span class="sxs-lookup"><span data-stu-id="94e63-179">Specifies the job under which this cmdlet creates the task.</span></span>
<span data-ttu-id="94e63-180">Чтобы получить объект **PSCloudJob** , используйте командлет Get-AzBatchJob.</span><span class="sxs-lookup"><span data-stu-id="94e63-180">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="94e63-181">-JobId</span><span class="sxs-lookup"><span data-stu-id="94e63-181">-JobId</span></span>
<span data-ttu-id="94e63-182">Указывает идентификатор задания, в рамках которого этот командлет создает задачу.</span><span class="sxs-lookup"><span data-stu-id="94e63-182">Specifies the ID of the job under which this cmdlet creates the task.</span></span>

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

### <span data-ttu-id="94e63-183">-MultiInstanceSettings</span><span class="sxs-lookup"><span data-stu-id="94e63-183">-MultiInstanceSettings</span></span>
<span data-ttu-id="94e63-184">Задает сведения о том, как выполнить задачу с несколькими экземплярами.</span><span class="sxs-lookup"><span data-stu-id="94e63-184">Specifies information about how to run a multi-instance task.</span></span>

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

### <span data-ttu-id="94e63-185">-Выходной_файл</span><span class="sxs-lookup"><span data-stu-id="94e63-185">-OutputFile</span></span>
<span data-ttu-id="94e63-186">Возвращает или задает список файлов, которые будут отправляться пакетной службой из COMPUTE node после выполнения командной строки.</span><span class="sxs-lookup"><span data-stu-id="94e63-186">Gets or sets a list of files that the Batch service will upload from the compute node after running the command line.</span></span>
<span data-ttu-id="94e63-187">Для задач с несколькими экземплярами файлы будут отправлены только из вычислительного узла, на котором выполняется основная задача.</span><span class="sxs-lookup"><span data-stu-id="94e63-187">For multi-instance tasks, the files will only be uploaded from the compute node on which the primary task is executed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSOutputFile[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94e63-188">-ResourceFiles</span><span class="sxs-lookup"><span data-stu-id="94e63-188">-ResourceFiles</span></span>
<span data-ttu-id="94e63-189">Определяет файлы ресурсов в виде пар "ключ-значение", которые требуются для задачи.</span><span class="sxs-lookup"><span data-stu-id="94e63-189">Specifies resource files, as key/value pairs, that the task requires.</span></span>
<span data-ttu-id="94e63-190">Key — путь к файлу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="94e63-190">The key is the resource file path.</span></span>
<span data-ttu-id="94e63-191">Значением является источник больших двоичных объектов файла ресурсов.</span><span class="sxs-lookup"><span data-stu-id="94e63-191">The value is the resource file blob source.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: JobId_Single, JobObject_Single
Aliases: ResourceFile

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94e63-192">-Задачи</span><span class="sxs-lookup"><span data-stu-id="94e63-192">-Tasks</span></span>
<span data-ttu-id="94e63-193">Указывает коллекцию задач, которые нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="94e63-193">Specifies the collection of tasks to be added.</span></span>
<span data-ttu-id="94e63-194">Каждая задача должна иметь уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="94e63-194">Each task must have a unique ID.</span></span>

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

### <span data-ttu-id="94e63-195">-UserIdentity</span><span class="sxs-lookup"><span data-stu-id="94e63-195">-UserIdentity</span></span>
<span data-ttu-id="94e63-196">Учетная запись пользователя, под которой запускается задача.</span><span class="sxs-lookup"><span data-stu-id="94e63-196">The user identity under which the task runs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSUserIdentity
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94e63-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94e63-197">CommonParameters</span></span>
<span data-ttu-id="94e63-198">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="94e63-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94e63-199">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94e63-199">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94e63-200">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="94e63-200">INPUTS</span></span>

### <span data-ttu-id="94e63-201">Microsoft.Azure.Commands.BatCH. Models. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="94e63-201">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="94e63-202">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="94e63-202">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="94e63-203">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="94e63-203">OUTPUTS</span></span>

### <span data-ttu-id="94e63-204">System. void</span><span class="sxs-lookup"><span data-stu-id="94e63-204">System.Void</span></span>

## <span data-ttu-id="94e63-205">Пуск</span><span class="sxs-lookup"><span data-stu-id="94e63-205">NOTES</span></span>

## <span data-ttu-id="94e63-206">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="94e63-206">RELATED LINKS</span></span>

[<span data-ttu-id="94e63-207">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="94e63-207">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="94e63-208">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="94e63-208">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="94e63-209">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="94e63-209">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="94e63-210">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="94e63-210">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="94e63-211">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="94e63-211">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="94e63-212">Остановить-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="94e63-212">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="94e63-213">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="94e63-213">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


