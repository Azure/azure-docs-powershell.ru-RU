---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2B4BFDDA-9721-42E6-84E1-A209CB782954
online version: https://docs.microsoft.com/powershell/module/az.batch/new-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchTask.md
ms.openlocfilehash: 254c9290b2cc838dc7ec53c2590d8505c24c1b69
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992956"
---
# <span data-ttu-id="61aaa-101">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="61aaa-101">New-AzBatchTask</span></span>

## <span data-ttu-id="61aaa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61aaa-102">SYNOPSIS</span></span>
<span data-ttu-id="61aaa-103">Создает пакетную задачу для задания.</span><span class="sxs-lookup"><span data-stu-id="61aaa-103">Creates a Batch task under a job.</span></span>

## <span data-ttu-id="61aaa-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="61aaa-104">SYNTAX</span></span>

### <span data-ttu-id="61aaa-105">JobId_Single (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="61aaa-105">JobId_Single (Default)</span></span>
```
New-AzBatchTask -JobId <String> -Id <String> [-DisplayName <String>] -CommandLine <String>
 [-ResourceFiles <PSResourceFile[]>] [-EnvironmentSettings <IDictionary>]
 [-AuthenticationTokenSettings <PSAuthenticationTokenSettings>] [-UserIdentity <PSUserIdentity>]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-OutputFile <PSOutputFile[]>]
 [-ExitConditions <PSExitConditions>] [-ContainerSettings <PSTaskContainerSettings>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61aaa-106">JobId_Bulk</span><span class="sxs-lookup"><span data-stu-id="61aaa-106">JobId_Bulk</span></span>
```
New-AzBatchTask -JobId <String> [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61aaa-107">JobObject_Bulk</span><span class="sxs-lookup"><span data-stu-id="61aaa-107">JobObject_Bulk</span></span>
```
New-AzBatchTask [-Job <PSCloudJob>] [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61aaa-108">JobObject_Single</span><span class="sxs-lookup"><span data-stu-id="61aaa-108">JobObject_Single</span></span>
```
New-AzBatchTask [-Job <PSCloudJob>] -Id <String> [-DisplayName <String>] -CommandLine <String>
 [-ResourceFiles <PSResourceFile[]>] [-EnvironmentSettings <IDictionary>]
 [-AuthenticationTokenSettings <PSAuthenticationTokenSettings>] [-UserIdentity <PSUserIdentity>]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-OutputFile <PSOutputFile[]>]
 [-ExitConditions <PSExitConditions>] [-ContainerSettings <PSTaskContainerSettings>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61aaa-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="61aaa-109">DESCRIPTION</span></span>
<span data-ttu-id="61aaa-110">Для **задания,** заданного параметром JobId или параметром *JobId,* создается задача  Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="61aaa-110">The **New-AzBatchTask** cmdlet creates an Azure Batch task under the job specified by the *JobId* parameter or the *Job* parameter.</span></span>

## <span data-ttu-id="61aaa-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="61aaa-111">EXAMPLES</span></span>

### <span data-ttu-id="61aaa-112">Пример 1. Создание пакетной задачи</span><span class="sxs-lookup"><span data-stu-id="61aaa-112">Example 1: Create a Batch task</span></span>
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
```

<span data-ttu-id="61aaa-113">Эта команда создает задачу с ИД задачи23 для задания с заданием 0000001.</span><span class="sxs-lookup"><span data-stu-id="61aaa-113">This command creates a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="61aaa-114">Задача выполняет указанную команду.</span><span class="sxs-lookup"><span data-stu-id="61aaa-114">The task runs the specified command.</span></span>
<span data-ttu-id="61aaa-115">Чтобы назначить контекст переменной $Context, используйте $Context **AzBatchAccountKey.**</span><span class="sxs-lookup"><span data-stu-id="61aaa-115">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="61aaa-116">Пример 2. Создание пакетной задачи</span><span class="sxs-lookup"><span data-stu-id="61aaa-116">Example 2: Create a Batch task</span></span>
```
PS C:\> $autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
PS C:\> $userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
PS C:\>Get-AzBatchJob -Id "Job-000001" -BatchContext $Context | New-AzBatchTask -Id "Task26" -CommandLine "cmd /c echo hello > newFile.txt" -UserIdentity $userIdentity -BatchContext $Context
```

<span data-ttu-id="61aaa-117">Эта команда получает задание пакета с заданием для задания ID-000001 с помощью командлета **Get-AzBatchJob.**</span><span class="sxs-lookup"><span data-stu-id="61aaa-117">This command gets the Batch job that has the ID Job-000001 by using the **Get-AzBatchJob** cmdlet.</span></span>
<span data-ttu-id="61aaa-118">Эта команда передает это задание текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="61aaa-118">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="61aaa-119">Эта команда создает задачу с ид. задачей26 для этого задания.</span><span class="sxs-lookup"><span data-stu-id="61aaa-119">The command creates a task that has the ID Task26 under that job.</span></span>
<span data-ttu-id="61aaa-120">Задача выполняет указанную команду с повышенными разрешениями.</span><span class="sxs-lookup"><span data-stu-id="61aaa-120">The task runs the specified command by using elevated permissions.</span></span>

### <span data-ttu-id="61aaa-121">Пример 3. Добавление коллекции задач в указанное задание с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="61aaa-121">Example 3: Add a collection of tasks to the specified job by using the pipeline</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> Get-AzBatchJob -Id "Job-000001" -BatchContext $Context | New-AzBatchTask -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="61aaa-122">Первая команда создает ссылку на ключи учетных записей для пакетной учетной записи ContosoBatchAccount с помощью **Get-AzBatchAccountKey.**</span><span class="sxs-lookup"><span data-stu-id="61aaa-122">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="61aaa-123">Эта ссылка на объект сохраняется в переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="61aaa-123">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="61aaa-124">Следующие две команды создают **объекты PSCloudTask** с помощью New-Object командлета.</span><span class="sxs-lookup"><span data-stu-id="61aaa-124">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="61aaa-125">Команды сохраняют задачи в переменных $Task 01 и $Task 02.</span><span class="sxs-lookup"><span data-stu-id="61aaa-125">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>
<span data-ttu-id="61aaa-126">Конечная команда получает задание пакета с заданием для работы с ИД-000001 с помощью **Get-AzBatchJob.**</span><span class="sxs-lookup"><span data-stu-id="61aaa-126">The final command gets the Batch job that has the ID Job-000001 by using **Get-AzBatchJob**.</span></span>
<span data-ttu-id="61aaa-127">Затем команда передает это задание текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="61aaa-127">Then the command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="61aaa-128">Эта команда добавляет набор задач в рамках этого задания.</span><span class="sxs-lookup"><span data-stu-id="61aaa-128">The command adds a collection of tasks under that job.</span></span>
<span data-ttu-id="61aaa-129">Для этой команды используется контекст, сохраненный в $Context.</span><span class="sxs-lookup"><span data-stu-id="61aaa-129">The command uses the context stored in $Context.</span></span>

### <span data-ttu-id="61aaa-130">Пример 4. Добавление коллекции задач к указанному заданию</span><span class="sxs-lookup"><span data-stu-id="61aaa-130">Example 4: Add a collection of tasks to the specified job</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> New-AzBatchTask -JobId "Job-000001" -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="61aaa-131">Первая команда создает ссылку на ключи учетных записей для пакетной учетной записи ContosoBatchAccount с помощью **Get-AzBatchAccountKey.**</span><span class="sxs-lookup"><span data-stu-id="61aaa-131">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="61aaa-132">Эта ссылка на объект сохраняется в переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="61aaa-132">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="61aaa-133">Следующие две команды создают **объекты PSCloudTask** с помощью New-Object командлета.</span><span class="sxs-lookup"><span data-stu-id="61aaa-133">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="61aaa-134">Команды сохраняют задачи в переменных $Task 01 и $Task 02.</span><span class="sxs-lookup"><span data-stu-id="61aaa-134">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>
<span data-ttu-id="61aaa-135">Конечная команда добавляет задачи, хранимые в $Task 01 и $Task 02, в рамках задания с ИД-000001.</span><span class="sxs-lookup"><span data-stu-id="61aaa-135">The final command adds the tasks stored in $Task01 and $Task02 under the job that has the ID Job-000001.</span></span>

### <span data-ttu-id="61aaa-136">Пример 5. Добавление задачи с выходными файлами</span><span class="sxs-lookup"><span data-stu-id="61aaa-136">Example 5: Add a task with output files</span></span>
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
PS C:\>$blobContainerDestination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileBlobContainerDestination "https://myaccount.blob.core.windows.net/sascontainer?sv=2015-04-05&st=2015-04-29T22%3A18%3A26Z&se=2015-04-30T02%3A23%3A26Z&sr=b&sp=rw&spr=https&sig=Z%2FRHIX5Xcg0Mq2rqI3OlWTjEg2tYkboXr1P9ZUXDtkk%3D"
PS C:\>$destination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileDestination $blobContainerDestination
PS C:\>$uploadOptions = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileUploadOptions "TaskSuccess"
PS C:\>$outputFile = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFile "*.txt", $blobContainerDestination, $uploadOptions

PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -OutputFile $outputFile -BatchContext $Context
```

### <span data-ttu-id="61aaa-137">Пример 6. Добавление задачи с помощью параметров маркера проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="61aaa-137">Example 6: Add a task with authentication token settings</span></span>
```
PS C:\>$authSettings = New-Object Microsoft.Azure.Commands.Batch.Models.PSAuthenticationTokenSettings
PS C:\>$authSettings.Access = "Job"
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -AuthenticationTokenSettings $authSettings -BatchContext $Context
```

### <span data-ttu-id="61aaa-138">Пример 7. Добавление задачи, которая выполняется в контейнере</span><span class="sxs-lookup"><span data-stu-id="61aaa-138">Example 7: Add a task which runs in a container</span></span>
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ContainerSettings New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskContainerSettings "containerImageName"
```

## <span data-ttu-id="61aaa-139">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61aaa-139">PARAMETERS</span></span>

### <span data-ttu-id="61aaa-140">-AffinityInformation</span><span class="sxs-lookup"><span data-stu-id="61aaa-140">-AffinityInformation</span></span>
<span data-ttu-id="61aaa-141">Указывает подсказку о локальности, которую служба обработки пакетов использует для выбора узла, на котором нужно выполнить задачу.</span><span class="sxs-lookup"><span data-stu-id="61aaa-141">Specifies a locality hint that the Batch service uses to select a node on which to run the task.</span></span>

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

### <span data-ttu-id="61aaa-142">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="61aaa-142">-ApplicationPackageReferences</span></span>
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

### <span data-ttu-id="61aaa-143">-AuthenticationTokenSettings</span><span class="sxs-lookup"><span data-stu-id="61aaa-143">-AuthenticationTokenSettings</span></span>
<span data-ttu-id="61aaa-144">Параметры маркера проверки подлинности, который можно использовать для выполнения пакетных операций службы.</span><span class="sxs-lookup"><span data-stu-id="61aaa-144">The settings for an authentication token that the task can use to perform Batch service operations.</span></span>
<span data-ttu-id="61aaa-145">Если этот запрос за установлен, служба обработки пакетов предоставляет задаче маркер проверки подлинности, который можно использовать для проверки подлинности пакетной службы без запроса ключа доступа к учетной записи.</span><span class="sxs-lookup"><span data-stu-id="61aaa-145">If this is set, the Batch service provides the task with an authentication token which can be used to authenticate Batch service operations without requiring an account access key.</span></span> <span data-ttu-id="61aaa-146">Маркер предоставляется с помощью переменной AZ_BATCH_AUTHENTICATION_TOKEN среды.</span><span class="sxs-lookup"><span data-stu-id="61aaa-146">The token is provided via the AZ_BATCH_AUTHENTICATION_TOKEN environment variable.</span></span> <span data-ttu-id="61aaa-147">Операции, которые можно выполнить с помощью маркера, зависят от параметров.</span><span class="sxs-lookup"><span data-stu-id="61aaa-147">The operations that the task can carry out using the token depend on the settings.</span></span> <span data-ttu-id="61aaa-148">Например, задача может запросить разрешение на выполнение задания, чтобы добавить к заданию другие задачи или проверить состояние задания или других задач.</span><span class="sxs-lookup"><span data-stu-id="61aaa-148">For example, a task can request job permissions in order to add other tasks to the job, or check the status of the job or of other tasks.</span></span>

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

### <span data-ttu-id="61aaa-149">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="61aaa-149">-BatchContext</span></span>
<span data-ttu-id="61aaa-150">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="61aaa-150">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="61aaa-151">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой пакета будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="61aaa-151">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="61aaa-152">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="61aaa-152">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="61aaa-153">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="61aaa-153">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="61aaa-154">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="61aaa-154">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="61aaa-155">-CommandLine</span><span class="sxs-lookup"><span data-stu-id="61aaa-155">-CommandLine</span></span>
<span data-ttu-id="61aaa-156">Определяет командную строку для задачи.</span><span class="sxs-lookup"><span data-stu-id="61aaa-156">Specifies the command line for the task.</span></span>

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

### <span data-ttu-id="61aaa-157">-Ограничения</span><span class="sxs-lookup"><span data-stu-id="61aaa-157">-Constraints</span></span>
<span data-ttu-id="61aaa-158">Определяет ограничения выполнения, которые применяются к данной задаче.</span><span class="sxs-lookup"><span data-stu-id="61aaa-158">Specifies the execution constraints that apply to this task.</span></span>

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

### <span data-ttu-id="61aaa-159">-ContainerSettings</span><span class="sxs-lookup"><span data-stu-id="61aaa-159">-ContainerSettings</span></span>
<span data-ttu-id="61aaa-160">Параметры контейнера, под которым выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="61aaa-160">The settings for the container under which the task runs.</span></span>
<span data-ttu-id="61aaa-161">Если у пула, который будет запускать эту задачу, есть набор контейнеровConfiguration, это также необходимо сделать.</span><span class="sxs-lookup"><span data-stu-id="61aaa-161">If the pool that will run this task has containerConfiguration set, this must be set as well.</span></span> <span data-ttu-id="61aaa-162">Если у пула, который будет выполнить эту задачу, нет набора контейнеровConfiguration, это не обязательно.</span><span class="sxs-lookup"><span data-stu-id="61aaa-162">If the pool that will run this task doesn't have containerConfiguration set, this must not be set.</span></span> <span data-ttu-id="61aaa-163">Если этот параметр задан, все каталоги, которые рекурсивно находятся под каталогом AZ_BATCH_NODE_ROOT_DIR (корневые каталоги пакетов Azure на узле), соединятся с контейнером, все переменные среды задач будут соединяться в контейнере, а в контейнере будет выполняться строка команд задачи.</span><span class="sxs-lookup"><span data-stu-id="61aaa-163">When this is specified, all directories recursively below the AZ_BATCH_NODE_ROOT_DIR (the root of Azure Batch directories on the node) are mapped into the container, all task environment variables are mapped into the container, and the task command line is executed in the container.</span></span>

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

### <span data-ttu-id="61aaa-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61aaa-164">-DefaultProfile</span></span>
<span data-ttu-id="61aaa-165">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="61aaa-165">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61aaa-166">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="61aaa-166">-DependsOn</span></span>
<span data-ttu-id="61aaa-167">Указывает, что задача зависит от других задач.</span><span class="sxs-lookup"><span data-stu-id="61aaa-167">Specifies that the task depends on other tasks.</span></span>
<span data-ttu-id="61aaa-168">Задача не будет запланирована до успешного завершения всех зависят от задач.</span><span class="sxs-lookup"><span data-stu-id="61aaa-168">The task will not be scheduled until all depended-on tasks have completed successfully.</span></span>

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

### <span data-ttu-id="61aaa-169">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="61aaa-169">-DisplayName</span></span>
<span data-ttu-id="61aaa-170">Отображает имя задачи.</span><span class="sxs-lookup"><span data-stu-id="61aaa-170">Specifies the display name of the task.</span></span>

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

### <span data-ttu-id="61aaa-171">-EnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="61aaa-171">-EnvironmentSettings</span></span>
<span data-ttu-id="61aaa-172">Определяет параметры среды в качестве пар ключа и значения, которые этот cmdlet добавляет к задаче.</span><span class="sxs-lookup"><span data-stu-id="61aaa-172">Specifies the environment settings, as key/value pairs, that this cmdlet adds to the task.</span></span>
<span data-ttu-id="61aaa-173">Ключом является имя параметра среды.</span><span class="sxs-lookup"><span data-stu-id="61aaa-173">The key is the environment setting name.</span></span>
<span data-ttu-id="61aaa-174">Значение — это параметр среды.</span><span class="sxs-lookup"><span data-stu-id="61aaa-174">The value is the environment setting.</span></span>

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

### <span data-ttu-id="61aaa-175">-ExitConditions</span><span class="sxs-lookup"><span data-stu-id="61aaa-175">-ExitConditions</span></span>
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

### <span data-ttu-id="61aaa-176">-Id</span><span class="sxs-lookup"><span data-stu-id="61aaa-176">-Id</span></span>
<span data-ttu-id="61aaa-177">Определяет ИД задачи.</span><span class="sxs-lookup"><span data-stu-id="61aaa-177">Specifies the ID of the task.</span></span>

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

### <span data-ttu-id="61aaa-178">-Job</span><span class="sxs-lookup"><span data-stu-id="61aaa-178">-Job</span></span>
<span data-ttu-id="61aaa-179">Задание, для которого этот cmdlet создает задачу.</span><span class="sxs-lookup"><span data-stu-id="61aaa-179">Specifies the job under which this cmdlet creates the task.</span></span>
<span data-ttu-id="61aaa-180">Чтобы получить объект **PSCloudJob,** используйте Get-AzBatchJob.</span><span class="sxs-lookup"><span data-stu-id="61aaa-180">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="61aaa-181">-JobId</span><span class="sxs-lookup"><span data-stu-id="61aaa-181">-JobId</span></span>
<span data-ttu-id="61aaa-182">Определяет код задания, в котором этот cmdlet создает задачу.</span><span class="sxs-lookup"><span data-stu-id="61aaa-182">Specifies the ID of the job under which this cmdlet creates the task.</span></span>

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

### <span data-ttu-id="61aaa-183">-MultiInstanceSettings</span><span class="sxs-lookup"><span data-stu-id="61aaa-183">-MultiInstanceSettings</span></span>
<span data-ttu-id="61aaa-184">Указывает сведения о том, как выполнить задачу с несколькими экземплярами.</span><span class="sxs-lookup"><span data-stu-id="61aaa-184">Specifies information about how to run a multi-instance task.</span></span>

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

### <span data-ttu-id="61aaa-185">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="61aaa-185">-OutputFile</span></span>
<span data-ttu-id="61aaa-186">Возвращает или задает список файлов, которые служба batch'' будет загружать с узла компьютеров после запуска командной строки.</span><span class="sxs-lookup"><span data-stu-id="61aaa-186">Gets or sets a list of files that the Batch service will upload from the compute node after running the command line.</span></span>
<span data-ttu-id="61aaa-187">Для задач с несколькими экземплярами файлы загружаются только с узла компьютеров, на котором выполняется основная задача.</span><span class="sxs-lookup"><span data-stu-id="61aaa-187">For multi-instance tasks, the files will only be uploaded from the compute node on which the primary task is executed.</span></span>

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

### <span data-ttu-id="61aaa-188">-ResourceFiles</span><span class="sxs-lookup"><span data-stu-id="61aaa-188">-ResourceFiles</span></span>
<span data-ttu-id="61aaa-189">Определяет файлы ресурсов в качестве пар ключа и значения, необходимых для задачи.</span><span class="sxs-lookup"><span data-stu-id="61aaa-189">Specifies resource files, as key/value pairs, that the task requires.</span></span>
<span data-ttu-id="61aaa-190">Ключом является путь к файлу ресурса.</span><span class="sxs-lookup"><span data-stu-id="61aaa-190">The key is the resource file path.</span></span>
<span data-ttu-id="61aaa-191">Значение — это источник BLOB-файлов ресурсов.</span><span class="sxs-lookup"><span data-stu-id="61aaa-191">The value is the resource file blob source.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSResourceFile[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases: ResourceFile

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61aaa-192">-Задачи</span><span class="sxs-lookup"><span data-stu-id="61aaa-192">-Tasks</span></span>
<span data-ttu-id="61aaa-193">Набор добавляемых задач.</span><span class="sxs-lookup"><span data-stu-id="61aaa-193">Specifies the collection of tasks to be added.</span></span>
<span data-ttu-id="61aaa-194">У каждой задачи должен быть уникальный ИД.</span><span class="sxs-lookup"><span data-stu-id="61aaa-194">Each task must have a unique ID.</span></span>

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

### <span data-ttu-id="61aaa-195">-UserIdentity</span><span class="sxs-lookup"><span data-stu-id="61aaa-195">-UserIdentity</span></span>
<span data-ttu-id="61aaa-196">Идентификатор пользователя, под которым выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="61aaa-196">The user identity under which the task runs.</span></span>

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

### <span data-ttu-id="61aaa-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61aaa-197">CommonParameters</span></span>
<span data-ttu-id="61aaa-198">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61aaa-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61aaa-199">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="61aaa-199">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61aaa-200">INPUTS</span><span class="sxs-lookup"><span data-stu-id="61aaa-200">INPUTS</span></span>

### <span data-ttu-id="61aaa-201">Microsoft.Azure.Commands.Batch. Models.PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="61aaa-201">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="61aaa-202">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="61aaa-202">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="61aaa-203">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="61aaa-203">OUTPUTS</span></span>

### <span data-ttu-id="61aaa-204">System.Void</span><span class="sxs-lookup"><span data-stu-id="61aaa-204">System.Void</span></span>

## <span data-ttu-id="61aaa-205">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="61aaa-205">NOTES</span></span>

## <span data-ttu-id="61aaa-206">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="61aaa-206">RELATED LINKS</span></span>

[<span data-ttu-id="61aaa-207">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="61aaa-207">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="61aaa-208">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="61aaa-208">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="61aaa-209">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="61aaa-209">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="61aaa-210">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="61aaa-210">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="61aaa-211">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="61aaa-211">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="61aaa-212">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="61aaa-212">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="61aaa-213">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="61aaa-213">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
