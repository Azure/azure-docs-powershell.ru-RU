---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 38ED2854-23D0-400E-A5C8-239346B2AF99
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchnodefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFile.md
ms.openlocfilehash: db8ef62a158edaa3a697af9f77e7932dfa18c096
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398279"
---
# <span data-ttu-id="3b8b1-101">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="3b8b1-101">Get-AzBatchNodeFile</span></span>

## <span data-ttu-id="3b8b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b8b1-102">SYNOPSIS</span></span>
<span data-ttu-id="3b8b1-103">Свойства пакетных файлов узлов.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-103">Gets the properties of Batch node files.</span></span>

## <span data-ttu-id="3b8b1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3b8b1-104">SYNTAX</span></span>

### <span data-ttu-id="3b8b1-105">ComputeNode_Id (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3b8b1-105">ComputeNode_Id (Default)</span></span>
```
Get-AzBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> [[-Path] <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b8b1-106">Task_Id</span><span class="sxs-lookup"><span data-stu-id="3b8b1-106">Task_Id</span></span>
```
Get-AzBatchNodeFile -JobId <String> -TaskId <String> [[-Path] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b8b1-107">Task_ODataFilter</span><span class="sxs-lookup"><span data-stu-id="3b8b1-107">Task_ODataFilter</span></span>
```
Get-AzBatchNodeFile -JobId <String> -TaskId <String> [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b8b1-108">ParentTask</span><span class="sxs-lookup"><span data-stu-id="3b8b1-108">ParentTask</span></span>
```
Get-AzBatchNodeFile [[-Task] <PSCloudTask>] [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b8b1-109">ComputeNode_ODataFilter</span><span class="sxs-lookup"><span data-stu-id="3b8b1-109">ComputeNode_ODataFilter</span></span>
```
Get-AzBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Recursive] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3b8b1-110">ParentComputeNode</span><span class="sxs-lookup"><span data-stu-id="3b8b1-110">ParentComputeNode</span></span>
```
Get-AzBatchNodeFile [[-ComputeNode] <PSComputeNode>] [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b8b1-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b8b1-111">DESCRIPTION</span></span>
<span data-ttu-id="3b8b1-112">С **его использованием** можно получить свойства пакетных файлов узла Azure для узла задачи или узла вычислений.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-112">The **Get-AzBatchNodeFile** cmdlet gets the properties of the Azure Batch node files of a task or compute node.</span></span>
<span data-ttu-id="3b8b1-113">Чтобы сузить результаты, можно указать фильтр OData.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-113">To narrow your results, you can specify an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="3b8b1-114">Если вы указали задачу, но не фильтр, этот cmdlet возвращает свойства для всех файлов узлов для этой задачи.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-114">If you specify a task, but not a filter, this cmdlet returns properties for all node files for that task.</span></span>
<span data-ttu-id="3b8b1-115">Если указать узел вычислений, но не фильтр, этот cmdlet возвратит свойства для всех файлов узла для этого узла.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-115">If you specify a compute node, but not a filter, this cmdlet returns properties for all node files for that compute node.</span></span>

## <span data-ttu-id="3b8b1-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3b8b1-116">EXAMPLES</span></span>

### <span data-ttu-id="3b8b1-117">Пример 1. Просмотр свойств файла узла, связанного с задачей</span><span class="sxs-lookup"><span data-stu-id="3b8b1-117">Example 1: Get the properties of a node file associated with a task</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "Stdout.txt" -BatchContext $Context
IsDirectory Name          Properties                                      Url

----------- ----          ----------                                      ---

False       StdOut.txt    Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="3b8b1-118">Эта команда получает свойства файла узла StdOut.txt, связанного с задачей, которая имеет задачу "ИД задачи26" для задания с ИД-000001.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-118">This command gets the properties of the StdOut.txt node file associated with the task that has the ID Task26 in the job that has the ID Job-000001.</span></span>
<span data-ttu-id="3b8b1-119">Используйте Get-AzBatchAccountKey для назначения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-119">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="3b8b1-120">Пример 2. Просмотр свойств файлов узлов, связанных с задачей, с помощью фильтра</span><span class="sxs-lookup"><span data-stu-id="3b8b1-120">Example 2: Get the properties of node files associated with a task by using a filter</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job-00002" -TaskId "Task26" -Filter "startswith(name,'St')" -BatchContext $Context
IsDirectory Name        Properties                                      Url

----------- ----        ----------                                      ---

False       StdErr.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
False       StdOut.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="3b8b1-121">Эта команда получает свойства файлов узла, имена которых начинаются с st и связаны с задачей, у которой есть задача ID Task26 в рамках задания с ИД-00002.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-121">This command gets the properties of the node files whose names start with st and are associated with task that has the ID Task26 under job that has the ID Job-00002.</span></span>

### <span data-ttu-id="3b8b1-122">Пример 3. Рекурсивно получите свойства файлов узлов, связанных с задачей</span><span class="sxs-lookup"><span data-stu-id="3b8b1-122">Example 3: Recursively get the properties of node files associated with a task</span></span>
```
PS C:\>Get-AzBatchTask "Job-00003" "Task31" -BatchContext $Context | Get-AzBatchNodeFile -Recursive -BatchContext $Context
IsDirectory Name             Properties                                      Url

----------- ----             ----------                                      ---

False       ProcessEnv.cmd   Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
False       StdErr.txt       Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
False       StdOut.txt       Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
True        wd                                                               https://cmdletexample.westus.Batch.contoso...
False       wd\newFile.txt   Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="3b8b1-123">Эта команда получает свойства всех файлов, связанных с задачей, которая имеет задачу "ID Task31" в job-00003.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-123">This command gets the properties of all files associated with the task that has the ID Task31 in job Job-00003.</span></span>
<span data-ttu-id="3b8b1-124">Эта команда определяет *рекурсивный* параметр.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-124">This command specifies the *Recursive* parameter.</span></span>
<span data-ttu-id="3b8b1-125">Таким образом, выполняется поиск рекурсивного файла и возвращается wd\newFile.txt узла.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-125">Therefore, the cmdlet performs a recursive file search is performed, and returns the wd\newFile.txt node file.</span></span>

### <span data-ttu-id="3b8b1-126">Пример 4. Получить один файл из узла вычислений</span><span class="sxs-lookup"><span data-stu-id="3b8b1-126">Example 4: Get a single file from a compute node</span></span>
```
PS C:\>Get-AzBatchNodeFile -PoolId "Pool22" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context
IsDirectory Name                    Properties                                      Url
----------- ----                    ----------                                      ---
False       startup\stdout.txt      Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="3b8b1-127">Эта команда получает файл с именем Startup\StdOut.txt из узла вычислений, в пуле которого есть ID ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-127">This command gets the file that is named Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>

### <span data-ttu-id="3b8b1-128">Пример 5. Все файлы, которые находятся в папке, можно получить из узла вычислений</span><span class="sxs-lookup"><span data-stu-id="3b8b1-128">Example 5: Get all files under a folder from a compute node</span></span>
```
PS C:\>Get-AzBatchNodeFile -PoolId "Pool22" -ComputeNodeId "ComputeNode01" -Filter "startswith(name,'startup')" -Recursive -BatchContext $Context
IsDirectory Name                      Properties                                      Url
----------- ----                      ----------                                      ---
True        startup                                                                   https://cmdletexample.westus.Batch.contoso...
False       startup\ProcessEnv.cmd    Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
False       startup\stderr.txt        Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
False       startup\stdout.txt        Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
True        startup\wd                                                                https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="3b8b1-129">Эта команда получает все файлы в папке запуска из узла вычислений, который содержит ID ComputeNode01 в пуле, который содержит ID Pool22.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-129">This command gets all the files under the startup folder from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>
<span data-ttu-id="3b8b1-130">Этот cmdlet указывает *рекурсивный* параметр.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-130">This cmdlet specifies the *Recursive* parameter.</span></span>

### <span data-ttu-id="3b8b1-131">Пример 6. Получить файлы из корневой папки узла вычислений</span><span class="sxs-lookup"><span data-stu-id="3b8b1-131">Example 6: Get files from the root folder of a compute node</span></span>
```
PS C:\>Get-AzBatchComputeNode "Pool22" -Id "ComputeNode01" -BatchContext $Context | Get-AzBatchNodeFile -BatchContext $Context
IsDirectory Name           Properties       Url
----------- ----           ----------       ---
True        shared                          https://cmdletexample.westus.Batch.contoso...
True        startup                         https://cmdletexample.westus.Batch.contoso...
True        workitems                       https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="3b8b1-132">Эта команда получает все файлы в корневой папке узла вычислений, в пуле с пулом, который содержит ID ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-132">This command gets all the files at the root folder of the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>

## <span data-ttu-id="3b8b1-133">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3b8b1-133">PARAMETERS</span></span>

### <span data-ttu-id="3b8b1-134">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="3b8b1-134">-BatchContext</span></span>
<span data-ttu-id="3b8b1-135">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-135">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="3b8b1-136">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой batchy будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-136">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="3b8b1-137">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-137">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="3b8b1-138">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-138">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="3b8b1-139">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-139">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="3b8b1-140">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="3b8b1-140">-ComputeNode</span></span>
<span data-ttu-id="3b8b1-141">Определяет узел вычислений в качестве объекта **PSComputeNode,** который содержит пакетные файлы узлов.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-141">Specifies the compute node, as a **PSComputeNode** object, that contains the Batch node files.</span></span>
<span data-ttu-id="3b8b1-142">Чтобы получить объект вычислительного узла, воспользуйтесь Get-AzBatchComputeNode..</span><span class="sxs-lookup"><span data-stu-id="3b8b1-142">To obtain a compute node object, use the Get-AzBatchComputeNode cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: ParentComputeNode
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b8b1-143">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="3b8b1-143">-ComputeNodeId</span></span>
<span data-ttu-id="3b8b1-144">Определяет ИД узла вычислений, который содержит пакетные файлы узлов.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-144">Specifies the ID of the compute node that contains the Batch node files.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id, ComputeNode_ODataFilter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b8b1-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b8b1-145">-DefaultProfile</span></span>
<span data-ttu-id="3b8b1-146">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b8b1-147">-Filter</span><span class="sxs-lookup"><span data-stu-id="3b8b1-147">-Filter</span></span>
<span data-ttu-id="3b8b1-148">Указывает предложение фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-148">Specifies an OData filter clause.</span></span>
<span data-ttu-id="3b8b1-149">Этот командлет возвращает свойства для файлов узлов, которые соответствуют фильтру, указанному этим параметром.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-149">This cmdlet returns properties for node files that match the filter that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_ODataFilter, ParentTask, ComputeNode_ODataFilter, ParentComputeNode
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b8b1-150">-JobId</span><span class="sxs-lookup"><span data-stu-id="3b8b1-150">-JobId</span></span>
<span data-ttu-id="3b8b1-151">Определяет ИД задания, которое содержит целевую задачу.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-151">Specifies the ID of the job that contains the target task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id, Task_ODataFilter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b8b1-152">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="3b8b1-152">-MaxCount</span></span>
<span data-ttu-id="3b8b1-153">Указывает максимальное количество файлов узлов, для которых этот cmdlet возвращает свойства.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-153">Specifies the maximum number of node files for which this cmdlet returns properties.</span></span>
<span data-ttu-id="3b8b1-154">Если указать нулевое (ноль) или меньшее значение, для cmdlet не используется верхний предел.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-154">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="3b8b1-155">Значение по умолчанию — 1000.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-155">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Task_ODataFilter, ParentTask, ComputeNode_ODataFilter, ParentComputeNode
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b8b1-156">-Path</span><span class="sxs-lookup"><span data-stu-id="3b8b1-156">-Path</span></span>
<span data-ttu-id="3b8b1-157">Путь к файлу узла, свойства которого извлекает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-157">Specifies the path of the node file for which this cmdlet retrieves properties.</span></span>
<span data-ttu-id="3b8b1-158">Поддиавные знаки указывать нельзя.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-158">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id, Task_Id
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b8b1-159">-PoolId</span><span class="sxs-lookup"><span data-stu-id="3b8b1-159">-PoolId</span></span>
<span data-ttu-id="3b8b1-160">Определяет ИД пула, который содержит узел вычислений, из которого можно получить свойства файлов узла.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-160">Specifies the ID of the pool that contains the compute node from which to get properties of node files.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id, ComputeNode_ODataFilter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b8b1-161">-Рекурсивное</span><span class="sxs-lookup"><span data-stu-id="3b8b1-161">-Recursive</span></span>
<span data-ttu-id="3b8b1-162">Указывает на то, что этот cmdlet возвращает рекурсивный список файлов.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-162">Indicates that this cmdlet returns a recursive list of files.</span></span>
<span data-ttu-id="3b8b1-163">В противном случае она возвращает только файлы из корневой папки.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-163">Otherwise, it returns only the files in the root folder.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Task_ODataFilter, ParentTask, ComputeNode_ODataFilter, ParentComputeNode
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b8b1-164">-Задача</span><span class="sxs-lookup"><span data-stu-id="3b8b1-164">-Task</span></span>
<span data-ttu-id="3b8b1-165">Указывает задачу как объект **PSCloudTask,** с которым связаны файлы узлов.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-165">Specifies the task, as a **PSCloudTask** object, with which the node files are associated.</span></span>
<span data-ttu-id="3b8b1-166">Чтобы получить объект задачи, воспользуйтесь Get-AzBatchTask..</span><span class="sxs-lookup"><span data-stu-id="3b8b1-166">To obtain a task object, use the Get-AzBatchTask cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: ParentTask
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b8b1-167">-TaskId</span><span class="sxs-lookup"><span data-stu-id="3b8b1-167">-TaskId</span></span>
<span data-ttu-id="3b8b1-168">Определяет код задачи, для которой этот cmdlet получает свойства файлов узлов.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-168">Specifies the ID of the task for which this cmdlet gets properties of node files.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id, Task_ODataFilter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b8b1-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b8b1-169">CommonParameters</span></span>
<span data-ttu-id="3b8b1-170">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b8b1-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b8b1-171">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3b8b1-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b8b1-172">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3b8b1-172">INPUTS</span></span>

### <span data-ttu-id="3b8b1-173">System.String</span><span class="sxs-lookup"><span data-stu-id="3b8b1-173">System.String</span></span>

### <span data-ttu-id="3b8b1-174">Microsoft.Azure.Commands.Batch. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="3b8b1-174">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="3b8b1-175">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="3b8b1-175">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="3b8b1-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="3b8b1-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="3b8b1-177">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3b8b1-177">OUTPUTS</span></span>

### <span data-ttu-id="3b8b1-178">Microsoft.Azure.Commands.Batch. Models.PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="3b8b1-178">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>

## <span data-ttu-id="3b8b1-179">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3b8b1-179">NOTES</span></span>

## <span data-ttu-id="3b8b1-180">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3b8b1-180">RELATED LINKS</span></span>

[<span data-ttu-id="3b8b1-181">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="3b8b1-181">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="3b8b1-182">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="3b8b1-182">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="3b8b1-183">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="3b8b1-183">Get-AzBatchNodeFileContent</span></span>](./Get-AzBatchNodeFileContent.md)

[<span data-ttu-id="3b8b1-184">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="3b8b1-184">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="3b8b1-185">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="3b8b1-185">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
