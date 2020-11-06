---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 2B4BFDDA-9721-42E6-84E1-A209CB782954
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchTask.md
ms.openlocfilehash: a081e6da07557033430033adc8ef28cb4b63da8c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561124"
---
# <span data-ttu-id="28111-101">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="28111-101">New-AzureBatchTask</span></span>

## <span data-ttu-id="28111-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="28111-102">SYNOPSIS</span></span>
<span data-ttu-id="28111-103">Создает пакетную задачу под заданием.</span><span class="sxs-lookup"><span data-stu-id="28111-103">Creates a Batch task under a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28111-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="28111-104">SYNTAX</span></span>

### <span data-ttu-id="28111-105">JobId_Single (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="28111-105">JobId_Single (Default)</span></span>
```
New-AzureBatchTask -JobId <String> -Id <String> [-DisplayName <String>] [-CommandLine <String>]
 [-ResourceFiles <IDictionary>] [-EnvironmentSettings <IDictionary>]
 [-AuthenticationTokenSettings <PSAuthenticationTokenSettings>] [-UserIdentity <PSUserIdentity>]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-OutputFile <PSOutputFile[]>]
 [-ExitConditions <PSExitConditions>] [-ContainerSettings <PSTaskContainerSettings>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28111-106">JobId_Bulk</span><span class="sxs-lookup"><span data-stu-id="28111-106">JobId_Bulk</span></span>
```
New-AzureBatchTask -JobId <String> [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28111-107">JobObject_Bulk</span><span class="sxs-lookup"><span data-stu-id="28111-107">JobObject_Bulk</span></span>
```
New-AzureBatchTask [-Job <PSCloudJob>] [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28111-108">JobObject_Single</span><span class="sxs-lookup"><span data-stu-id="28111-108">JobObject_Single</span></span>
```
New-AzureBatchTask [-Job <PSCloudJob>] -Id <String> [-DisplayName <String>] [-CommandLine <String>]
 [-ResourceFiles <IDictionary>] [-EnvironmentSettings <IDictionary>]
 [-AuthenticationTokenSettings <PSAuthenticationTokenSettings>] [-UserIdentity <PSUserIdentity>]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-OutputFile <PSOutputFile[]>]
 [-ExitConditions <PSExitConditions>] [-ContainerSettings <PSTaskContainerSettings>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28111-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="28111-109">DESCRIPTION</span></span>
<span data-ttu-id="28111-110">Командлет **New-AzureBatchTask** создает пакетную задачу Azure в задании, указанной параметром *JOBID* , или параметром *задания* .</span><span class="sxs-lookup"><span data-stu-id="28111-110">The **New-AzureBatchTask** cmdlet creates an Azure Batch task under the job specified by the *JobId* parameter or the *Job* parameter.</span></span>

## <span data-ttu-id="28111-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="28111-111">EXAMPLES</span></span>

### <span data-ttu-id="28111-112">Пример 1: создание пакетной задачи</span><span class="sxs-lookup"><span data-stu-id="28111-112">Example 1: Create a Batch task</span></span>
```
PS C:\>New-AzureBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
```

<span data-ttu-id="28111-113">Эта команда создает задачу с ИДЕНТИФИКАТОРом Task23 под заданием с ИДЕНТИФИКАТОРом задания 000001.</span><span class="sxs-lookup"><span data-stu-id="28111-113">This command creates a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="28111-114">Задача запускает указанную команду.</span><span class="sxs-lookup"><span data-stu-id="28111-114">The task runs the specified command.</span></span>
<span data-ttu-id="28111-115">Используйте командлет **Get-AzureRmBatchAccountKeys** , чтобы назначить контекст переменной $context.</span><span class="sxs-lookup"><span data-stu-id="28111-115">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="28111-116">Пример 2: создание пакетной задачи</span><span class="sxs-lookup"><span data-stu-id="28111-116">Example 2: Create a Batch task</span></span>
```
PS C:\> $autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
PS C:\> $userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
PS C:\>Get-AzureBatchJob -Id "Job-000001" -BatchContext $Context | New-AzureBatchTask -Id "Task26" -CommandLine "cmd /c echo hello > newFile.txt" -UserIdentity $userIdentity -BatchContext $Context
```

<span data-ttu-id="28111-117">Эта команда получает пакетное задание с ИД задания, 000001 с помощью командлета **Get-AzureBatchJob** .</span><span class="sxs-lookup"><span data-stu-id="28111-117">This command gets the Batch job that has the ID Job-000001 by using the **Get-AzureBatchJob** cmdlet.</span></span>
<span data-ttu-id="28111-118">Команда передает это задание текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="28111-118">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="28111-119">Команда создает задачу с ИДЕНТИФИКАТОРом Task26 под этим заданием.</span><span class="sxs-lookup"><span data-stu-id="28111-119">The command creates a task that has the ID Task26 under that job.</span></span>
<span data-ttu-id="28111-120">Задача выполняет указанную команду с повышенными разрешениями.</span><span class="sxs-lookup"><span data-stu-id="28111-120">The task runs the specified command by using elevated permissions.</span></span>

### <span data-ttu-id="28111-121">Пример 3: Добавление коллекции задач к указанному заданию с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="28111-121">Example 3: Add a collection of tasks to the specified job by using the pipeline</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> Get-AzureBatchJob -Id "Job-000001" -BatchContext $Context | New-AzureBatchTask -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="28111-122">Первая команда создает ссылку на объект для учетной записи пакетной службы с именем ContosoBatchAccount с помощью **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="28111-122">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="28111-123">Команда сохраняет ссылку на этот объект в переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="28111-123">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="28111-124">Следующие две команды создают объекты **PSCloudTask** с помощью командлета New-Object.</span><span class="sxs-lookup"><span data-stu-id="28111-124">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="28111-125">Команды хранят задачи в $Task 01 и $Task 02.</span><span class="sxs-lookup"><span data-stu-id="28111-125">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>
<span data-ttu-id="28111-126">Последняя команда получает пакетное задание с ИД задания 000001 с помощью **Get-AzureBatchJob**.</span><span class="sxs-lookup"><span data-stu-id="28111-126">The final command gets the Batch job that has the ID Job-000001 by using **Get-AzureBatchJob**.</span></span>
<span data-ttu-id="28111-127">Затем команда передает это задание текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="28111-127">Then the command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="28111-128">Команда добавляет коллекцию задач под этим заданием.</span><span class="sxs-lookup"><span data-stu-id="28111-128">The command adds a collection of tasks under that job.</span></span>
<span data-ttu-id="28111-129">Команда использует контекст, хранящийся в $Context.</span><span class="sxs-lookup"><span data-stu-id="28111-129">The command uses the context stored in $Context.</span></span>

### <span data-ttu-id="28111-130">Пример 4: Добавление коллекции задач к указанному заданию</span><span class="sxs-lookup"><span data-stu-id="28111-130">Example 4: Add a collection of tasks to the specified job</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> New-AzureBatchTask -JobId "Job-000001" -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="28111-131">Первая команда создает ссылку на объект для учетной записи пакетной службы с именем ContosoBatchAccount с помощью **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="28111-131">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="28111-132">Команда сохраняет ссылку на этот объект в переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="28111-132">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="28111-133">Следующие две команды создают объекты **PSCloudTask** с помощью командлета New-Object.</span><span class="sxs-lookup"><span data-stu-id="28111-133">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="28111-134">Команды хранят задачи в $Task 01 и $Task 02.</span><span class="sxs-lookup"><span data-stu-id="28111-134">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>
<span data-ttu-id="28111-135">Последняя команда добавляет задачи, которые хранятся в $Task 01 и $Task 02 под заданием с ИД задания 000001.</span><span class="sxs-lookup"><span data-stu-id="28111-135">The final command adds the tasks stored in $Task01 and $Task02 under the job that has the ID Job-000001.</span></span>

### <span data-ttu-id="28111-136">Пример 5: Добавление задачи с помощью выходных файлов</span><span class="sxs-lookup"><span data-stu-id="28111-136">Example 5: Add a task with output files</span></span>
```
PS C:\>New-AzureBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
PS C:\>$blobContainerDestination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileBlobContainerDestination "https://myaccount.blob.core.windows.net/sascontainer?sv=2015-04-05&st=2015-04-29T22%3A18%3A26Z&se=2015-04-30T02%3A23%3A26Z&sr=b&sp=rw&spr=https&sig=Z%2FRHIX5Xcg0Mq2rqI3OlWTjEg2tYkboXr1P9ZUXDtkk%3D"
PS C:\>$destination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileDestination $blobContainerDestination
PS C:\>$uploadOptions = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileUploadOptions "TaskSuccess"
PS C:\>$outputFile = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFile "*.txt", $blobContainerDestination, $uploadOptions

PS C:\>New-AzureBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -OutputFile $outputFile -BatchContext $Context
```

### <span data-ttu-id="28111-137">Пример 6: Добавление задачи с помощью параметров маркеров проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="28111-137">Example 6: Add a task with authentication token settings</span></span>
```
PS C:\>$authSettings = New-Object Microsoft.Azure.Commands.Batch.Models.PSAuthenticationTokenSettings
PS C:\>$authSettings.Access = "Job"
PS C:\>New-AzureBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -AuthenticationTokenSettings $authSettings -BatchContext $Context
```

### <span data-ttu-id="28111-138">Пример 7: Добавление задачи, выполняемой в контейнере</span><span class="sxs-lookup"><span data-stu-id="28111-138">Example 7: Add a task which runs in a container</span></span>
```
PS C:\>New-AzureBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ContainerSettings New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskContainerSettings "containerImageName"
```

## <span data-ttu-id="28111-139">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="28111-139">PARAMETERS</span></span>

### <span data-ttu-id="28111-140">-AffinityInformation</span><span class="sxs-lookup"><span data-stu-id="28111-140">-AffinityInformation</span></span>
<span data-ttu-id="28111-141">Указывает подсказку о расположении, которую служба Batch использует для выбора узла, на котором необходимо выполнить задачу.</span><span class="sxs-lookup"><span data-stu-id="28111-141">Specifies a locality hint that the Batch service uses to select a node on which to run the task.</span></span>

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

### <span data-ttu-id="28111-142">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="28111-142">-ApplicationPackageReferences</span></span>
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

### <span data-ttu-id="28111-143">-AuthenticationTokenSettings</span><span class="sxs-lookup"><span data-stu-id="28111-143">-AuthenticationTokenSettings</span></span>
<span data-ttu-id="28111-144">Параметры маркера проверки подлинности, который задача может использовать для выполнения операций пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="28111-144">The settings for an authentication token that the task can use to perform Batch service operations.</span></span>
<span data-ttu-id="28111-145">Если этот параметр задан, пакетная служба предоставляет задачу с маркером проверки подлинности, который можно использовать для проверки подлинности операций пакетной службы, не требуя ключа доступа учетной записи.</span><span class="sxs-lookup"><span data-stu-id="28111-145">If this is set, the Batch service provides the task with an authentication token which can be used to authenticate Batch service operations without requiring an account access key.</span></span> <span data-ttu-id="28111-146">Маркер предоставляется с помощью переменной среды AZ_BATCH_AUTHENTICATION_TOKEN.</span><span class="sxs-lookup"><span data-stu-id="28111-146">The token is provided via the AZ_BATCH_AUTHENTICATION_TOKEN environment variable.</span></span> <span data-ttu-id="28111-147">Операции, которые может выполнять задача с помощью маркера, зависят от параметров.</span><span class="sxs-lookup"><span data-stu-id="28111-147">The operations that the task can carry out using the token depend on the settings.</span></span> <span data-ttu-id="28111-148">Например, задача может запрашивать разрешения задания, чтобы добавить в задание другие задачи, или проверить состояние задания или других задач.</span><span class="sxs-lookup"><span data-stu-id="28111-148">For example, a task can request job permissions in order to add other tasks to the job, or check the status of the job or of other tasks.</span></span>

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

### <span data-ttu-id="28111-149">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="28111-149">-BatchContext</span></span>
<span data-ttu-id="28111-150">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="28111-150">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="28111-151">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="28111-151">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="28111-152">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="28111-152">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="28111-153">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="28111-153">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="28111-154">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="28111-154">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="28111-155">-CommandLine</span><span class="sxs-lookup"><span data-stu-id="28111-155">-CommandLine</span></span>
<span data-ttu-id="28111-156">Задает командную строку для задачи.</span><span class="sxs-lookup"><span data-stu-id="28111-156">Specifies the command line for the task.</span></span>

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

### <span data-ttu-id="28111-157">-Ограничения</span><span class="sxs-lookup"><span data-stu-id="28111-157">-Constraints</span></span>
<span data-ttu-id="28111-158">Указывает ограничения на выполнение, которые применяются к этой задаче.</span><span class="sxs-lookup"><span data-stu-id="28111-158">Specifies the execution constraints that apply to this task.</span></span>

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

### <span data-ttu-id="28111-159">-ContainerSettings</span><span class="sxs-lookup"><span data-stu-id="28111-159">-ContainerSettings</span></span>
<span data-ttu-id="28111-160">Параметры для контейнера, в котором выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="28111-160">The settings for the container under which the task runs.</span></span>
<span data-ttu-id="28111-161">Если для пула, на котором будет выполняться эта задача, задано значение containerConfiguration, оно также должно быть задано.</span><span class="sxs-lookup"><span data-stu-id="28111-161">If the pool that will run this task has containerConfiguration set, this must be set as well.</span></span> <span data-ttu-id="28111-162">Если для пула, на котором будет выполняться эта задача, не задан containerConfiguration, этот параметр не должен быть установлен.</span><span class="sxs-lookup"><span data-stu-id="28111-162">If the pool that will run this task doesn't have containerConfiguration set, this must not be set.</span></span> <span data-ttu-id="28111-163">Если задано значение, все каталоги, рекурсивно расположенные под AZ_BATCH_NODE_ROOT_DIR (корень пакетных папок Azure на узле), сопоставляются с контейнером, все переменные среды задач сопоставляются с контейнером, а Командная строка задачи выполняется в контейнере.</span><span class="sxs-lookup"><span data-stu-id="28111-163">When this is specified, all directories recursively below the AZ_BATCH_NODE_ROOT_DIR (the root of Azure Batch directories on the node) are mapped into the container, all task environment variables are mapped into the container, and the task command line is executed in the container.</span></span>

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

### <span data-ttu-id="28111-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28111-164">-DefaultProfile</span></span>
<span data-ttu-id="28111-165">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="28111-165">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28111-166">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="28111-166">-DependsOn</span></span>
<span data-ttu-id="28111-167">Указывает, что задача зависит от других задач.</span><span class="sxs-lookup"><span data-stu-id="28111-167">Specifies that the task depends on other tasks.</span></span>
<span data-ttu-id="28111-168">Задача не будет планироваться до тех пор, пока все зависимые задачи не будут выполнены успешно.</span><span class="sxs-lookup"><span data-stu-id="28111-168">The task will not be scheduled until all depended-on tasks have completed successfully.</span></span>

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

### <span data-ttu-id="28111-169">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="28111-169">-DisplayName</span></span>
<span data-ttu-id="28111-170">Указывает отображаемое имя задачи.</span><span class="sxs-lookup"><span data-stu-id="28111-170">Specifies the display name of the task.</span></span>

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

### <span data-ttu-id="28111-171">-EnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="28111-171">-EnvironmentSettings</span></span>
<span data-ttu-id="28111-172">Задает параметры среды в виде пар "ключ-значение", которые этот командлет добавляет к задаче.</span><span class="sxs-lookup"><span data-stu-id="28111-172">Specifies the environment settings, as key/value pairs, that this cmdlet adds to the task.</span></span>
<span data-ttu-id="28111-173">Ключом является имя параметра среды.</span><span class="sxs-lookup"><span data-stu-id="28111-173">The key is the environment setting name.</span></span>
<span data-ttu-id="28111-174">Значение является параметром среды.</span><span class="sxs-lookup"><span data-stu-id="28111-174">The value is the environment setting.</span></span>

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

### <span data-ttu-id="28111-175">-ExitConditions</span><span class="sxs-lookup"><span data-stu-id="28111-175">-ExitConditions</span></span>
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

### <span data-ttu-id="28111-176">-ID</span><span class="sxs-lookup"><span data-stu-id="28111-176">-Id</span></span>
<span data-ttu-id="28111-177">Указывает идентификатор задачи.</span><span class="sxs-lookup"><span data-stu-id="28111-177">Specifies the ID of the task.</span></span>

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

### <span data-ttu-id="28111-178">-Job</span><span class="sxs-lookup"><span data-stu-id="28111-178">-Job</span></span>
<span data-ttu-id="28111-179">Указывает задание, в рамках которого этот командлет создает задачу.</span><span class="sxs-lookup"><span data-stu-id="28111-179">Specifies the job under which this cmdlet creates the task.</span></span>
<span data-ttu-id="28111-180">Чтобы получить объект **PSCloudJob** , используйте командлет Get-AzureBatchJob.</span><span class="sxs-lookup"><span data-stu-id="28111-180">To obtain a **PSCloudJob** object, use the Get-AzureBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="28111-181">-JobId</span><span class="sxs-lookup"><span data-stu-id="28111-181">-JobId</span></span>
<span data-ttu-id="28111-182">Указывает идентификатор задания, в рамках которого этот командлет создает задачу.</span><span class="sxs-lookup"><span data-stu-id="28111-182">Specifies the ID of the job under which this cmdlet creates the task.</span></span>

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

### <span data-ttu-id="28111-183">-MultiInstanceSettings</span><span class="sxs-lookup"><span data-stu-id="28111-183">-MultiInstanceSettings</span></span>
<span data-ttu-id="28111-184">Задает сведения о том, как выполнить задачу с несколькими экземплярами.</span><span class="sxs-lookup"><span data-stu-id="28111-184">Specifies information about how to run a multi-instance task.</span></span>

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

### <span data-ttu-id="28111-185">-Выходной_файл</span><span class="sxs-lookup"><span data-stu-id="28111-185">-OutputFile</span></span>
<span data-ttu-id="28111-186">Возвращает или задает список файлов, которые будут отправляться пакетной службой из COMPUTE node после выполнения командной строки.</span><span class="sxs-lookup"><span data-stu-id="28111-186">Gets or sets a list of files that the Batch service will upload from the compute node after running the command line.</span></span>
<span data-ttu-id="28111-187">Для задач с несколькими экземплярами файлы будут отправлены только из вычислительного узла, на котором выполняется основная задача.</span><span class="sxs-lookup"><span data-stu-id="28111-187">For multi-instance tasks, the files will only be uploaded from the compute node on which the primary task is executed.</span></span>

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

### <span data-ttu-id="28111-188">-ResourceFiles</span><span class="sxs-lookup"><span data-stu-id="28111-188">-ResourceFiles</span></span>
<span data-ttu-id="28111-189">Определяет файлы ресурсов в виде пар "ключ-значение", которые требуются для задачи.</span><span class="sxs-lookup"><span data-stu-id="28111-189">Specifies resource files, as key/value pairs, that the task requires.</span></span>
<span data-ttu-id="28111-190">Key — путь к файлу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="28111-190">The key is the resource file path.</span></span>
<span data-ttu-id="28111-191">Значением является источник больших двоичных объектов файла ресурсов.</span><span class="sxs-lookup"><span data-stu-id="28111-191">The value is the resource file blob source.</span></span>

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

### <span data-ttu-id="28111-192">-Задачи</span><span class="sxs-lookup"><span data-stu-id="28111-192">-Tasks</span></span>
<span data-ttu-id="28111-193">Указывает коллекцию задач, которые нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="28111-193">Specifies the collection of tasks to be added.</span></span>
<span data-ttu-id="28111-194">Каждая задача должна иметь уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="28111-194">Each task must have a unique ID.</span></span>

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

### <span data-ttu-id="28111-195">-UserIdentity</span><span class="sxs-lookup"><span data-stu-id="28111-195">-UserIdentity</span></span>
<span data-ttu-id="28111-196">Учетная запись пользователя, под которой запускается задача.</span><span class="sxs-lookup"><span data-stu-id="28111-196">The user identity under which the task runs.</span></span>

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

### <span data-ttu-id="28111-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28111-197">CommonParameters</span></span>
<span data-ttu-id="28111-198">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="28111-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28111-199">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28111-199">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28111-200">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="28111-200">INPUTS</span></span>

### <span data-ttu-id="28111-201">Microsoft.Azure.Commands.BatCH. Models. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="28111-201">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>
<span data-ttu-id="28111-202">Параметры: Job (ByValue)</span><span class="sxs-lookup"><span data-stu-id="28111-202">Parameters: Job (ByValue)</span></span>

### <span data-ttu-id="28111-203">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="28111-203">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="28111-204">Параметры: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="28111-204">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="28111-205">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="28111-205">OUTPUTS</span></span>

### <span data-ttu-id="28111-206">System. void</span><span class="sxs-lookup"><span data-stu-id="28111-206">System.Void</span></span>

## <span data-ttu-id="28111-207">Пуск</span><span class="sxs-lookup"><span data-stu-id="28111-207">NOTES</span></span>

## <span data-ttu-id="28111-208">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="28111-208">RELATED LINKS</span></span>

[<span data-ttu-id="28111-209">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="28111-209">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="28111-210">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="28111-210">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="28111-211">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="28111-211">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="28111-212">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="28111-212">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="28111-213">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="28111-213">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="28111-214">Остановить-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="28111-214">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="28111-215">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="28111-215">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


