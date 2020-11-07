---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 38ED2854-23D0-400E-A5C8-239346B2AF99
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchnodefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFile.md
ms.openlocfilehash: 3337cfa2423d6bc3a26c96ea734ce517f2707a04
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93731879"
---
# <span data-ttu-id="d85ec-101">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="d85ec-101">Get-AzBatchNodeFile</span></span>

## <span data-ttu-id="d85ec-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d85ec-102">SYNOPSIS</span></span>
<span data-ttu-id="d85ec-103">Возвращает свойства файлов узлов пакета.</span><span class="sxs-lookup"><span data-stu-id="d85ec-103">Gets the properties of Batch node files.</span></span>

## <span data-ttu-id="d85ec-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d85ec-104">SYNTAX</span></span>

### <span data-ttu-id="d85ec-105">ComputeNode_Id (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d85ec-105">ComputeNode_Id (Default)</span></span>
```
Get-AzBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> [[-Path] <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d85ec-106">Task_Id</span><span class="sxs-lookup"><span data-stu-id="d85ec-106">Task_Id</span></span>
```
Get-AzBatchNodeFile -JobId <String> -TaskId <String> [[-Path] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d85ec-107">Task_ODataFilter</span><span class="sxs-lookup"><span data-stu-id="d85ec-107">Task_ODataFilter</span></span>
```
Get-AzBatchNodeFile -JobId <String> -TaskId <String> [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d85ec-108">ParentTask</span><span class="sxs-lookup"><span data-stu-id="d85ec-108">ParentTask</span></span>
```
Get-AzBatchNodeFile [[-Task] <PSCloudTask>] [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d85ec-109">ComputeNode_ODataFilter</span><span class="sxs-lookup"><span data-stu-id="d85ec-109">ComputeNode_ODataFilter</span></span>
```
Get-AzBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Recursive] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d85ec-110">ParentComputeNode</span><span class="sxs-lookup"><span data-stu-id="d85ec-110">ParentComputeNode</span></span>
```
Get-AzBatchNodeFile [[-ComputeNode] <PSComputeNode>] [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d85ec-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d85ec-111">DESCRIPTION</span></span>
<span data-ttu-id="d85ec-112">Командлет **Get-AzBatchNodeFile** получает свойства файлов пакетных узлов Azure для задачи или вычислительного узла.</span><span class="sxs-lookup"><span data-stu-id="d85ec-112">The **Get-AzBatchNodeFile** cmdlet gets the properties of the Azure Batch node files of a task or compute node.</span></span>
<span data-ttu-id="d85ec-113">Чтобы сузить результаты, вы можете указать фильтр протокола OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="d85ec-113">To narrow your results, you can specify an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="d85ec-114">Если вы укажете задачу, но не фильтр, этот командлет возвращает свойства для всех файлов узла для этой задачи.</span><span class="sxs-lookup"><span data-stu-id="d85ec-114">If you specify a task, but not a filter, this cmdlet returns properties for all node files for that task.</span></span>
<span data-ttu-id="d85ec-115">Если указать вычислительный узел, но не фильтр, этот командлет возвращает свойства для всех файлов узлов для этого вычислительного узла.</span><span class="sxs-lookup"><span data-stu-id="d85ec-115">If you specify a compute node, but not a filter, this cmdlet returns properties for all node files for that compute node.</span></span>

## <span data-ttu-id="d85ec-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d85ec-116">EXAMPLES</span></span>

### <span data-ttu-id="d85ec-117">Пример 1: получение свойств файла узла, связанного с задачей</span><span class="sxs-lookup"><span data-stu-id="d85ec-117">Example 1: Get the properties of a node file associated with a task</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "Stdout.txt" -BatchContext $Context
IsDirectory Name          Properties                                      Url

----------- ----          ----------                                      ---

False       StdOut.txt    Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="d85ec-118">Эта команда получает свойства файла узла StdOut.txt, связанного с задачей, которая имеет идентификатор Task26 в задании с ИД задания 000001.</span><span class="sxs-lookup"><span data-stu-id="d85ec-118">This command gets the properties of the StdOut.txt node file associated with the task that has the ID Task26 in the job that has the ID Job-000001.</span></span>
<span data-ttu-id="d85ec-119">Используйте командлет Get-AzBatchAccountKeys для присвоения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="d85ec-119">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="d85ec-120">Пример 2: получение свойств файлов узла, связанных с задачей с помощью фильтра</span><span class="sxs-lookup"><span data-stu-id="d85ec-120">Example 2: Get the properties of node files associated with a task by using a filter</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job-00002" -TaskId "Task26" -Filter "startswith(name,'St')" -BatchContext $Context
IsDirectory Name        Properties                                      Url

----------- ----        ----------                                      ---

False       StdErr.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       StdOut.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="d85ec-121">Эта команда получает свойства файлов узла, имена которых начинаются с ST и связанные с задачей, которая имеет идентификатор Task26 в разделе Задание с ИД задания 00002.</span><span class="sxs-lookup"><span data-stu-id="d85ec-121">This command gets the properties of the node files whose names start with st and are associated with task that has the ID Task26 under job that has the ID Job-00002.</span></span>

### <span data-ttu-id="d85ec-122">Пример 3: рекурсивное получение свойств файлов узлов, связанных с задачей</span><span class="sxs-lookup"><span data-stu-id="d85ec-122">Example 3: Recursively get the properties of node files associated with a task</span></span>
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

<span data-ttu-id="d85ec-123">Эта команда получает свойства всех файлов, связанных с задачей, которая имеет идентификатор Task31 в задании задания — 00003.</span><span class="sxs-lookup"><span data-stu-id="d85ec-123">This command gets the properties of all files associated with the task that has the ID Task31 in job Job-00003.</span></span>
<span data-ttu-id="d85ec-124">Эта команда задает *рекурсивный* параметр.</span><span class="sxs-lookup"><span data-stu-id="d85ec-124">This command specifies the *Recursive* parameter.</span></span>
<span data-ttu-id="d85ec-125">Таким образом, командлет выполняет рекурсивный поиск файла и возвращает файл узла wd\newFile.txt.</span><span class="sxs-lookup"><span data-stu-id="d85ec-125">Therefore, the cmdlet performs a recursive file search is performed, and returns the wd\newFile.txt node file.</span></span>

### <span data-ttu-id="d85ec-126">Пример 4: получение одного файла из вычислительного узла</span><span class="sxs-lookup"><span data-stu-id="d85ec-126">Example 4: Get a single file from a compute node</span></span>
```
PS C:\>Get-AzBatchNodeFile -PoolId "Pool22" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context
IsDirectory Name                    Properties                                      Url
----------- ----                    ----------                                      ---
False       startup\stdout.txt      Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="d85ec-127">Эта команда получает файл с именем Startup\StdOut.txt из COMPUTE Node, который имеет идентификатор ComputeNode01 в пуле с ИД Pool22.</span><span class="sxs-lookup"><span data-stu-id="d85ec-127">This command gets the file that is named Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>

### <span data-ttu-id="d85ec-128">Пример 5: получение всех файлов в папке с помощью вычислительного узла</span><span class="sxs-lookup"><span data-stu-id="d85ec-128">Example 5: Get all files under a folder from a compute node</span></span>
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

<span data-ttu-id="d85ec-129">Эта команда получает все файлы в папке "Автозагрузка" с узла COMPUTE node с ИД ComputeNode01 в пуле с ИД Pool22.</span><span class="sxs-lookup"><span data-stu-id="d85ec-129">This command gets all the files under the startup folder from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>
<span data-ttu-id="d85ec-130">Этот командлет задает *рекурсивный* параметр.</span><span class="sxs-lookup"><span data-stu-id="d85ec-130">This cmdlet specifies the *Recursive* parameter.</span></span>

### <span data-ttu-id="d85ec-131">Пример 6: получение файлов из корневой папки вычислительного узла</span><span class="sxs-lookup"><span data-stu-id="d85ec-131">Example 6: Get files from the root folder of a compute node</span></span>
```
PS C:\>Get-AzBatchComputeNode "Pool22" -Id "ComputeNode01" -BatchContext $Context | Get-AzBatchNodeFile -BatchContext $Context
IsDirectory Name           Properties       Url
----------- ----           ----------       ---
True        shared                          https://cmdletexample.westus.Batch.contoso... 
True        startup                         https://cmdletexample.westus.Batch.contoso... 
True        workitems                       https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="d85ec-132">Эта команда получает все файлы в корневой папке вычислительного узла с ИД ComputeNode01 в пуле с ИД Pool22.</span><span class="sxs-lookup"><span data-stu-id="d85ec-132">This command gets all the files at the root folder of the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>

## <span data-ttu-id="d85ec-133">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d85ec-133">PARAMETERS</span></span>

### <span data-ttu-id="d85ec-134">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d85ec-134">-BatchContext</span></span>
<span data-ttu-id="d85ec-135">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="d85ec-135">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d85ec-136">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="d85ec-136">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="d85ec-137">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="d85ec-137">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="d85ec-138">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="d85ec-138">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="d85ec-139">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="d85ec-139">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="d85ec-140">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="d85ec-140">-ComputeNode</span></span>
<span data-ttu-id="d85ec-141">Задает вычислительный узел как объект **PSComputeNode** , содержащий пакетные файлы узла.</span><span class="sxs-lookup"><span data-stu-id="d85ec-141">Specifies the compute node, as a **PSComputeNode** object, that contains the Batch node files.</span></span>
<span data-ttu-id="d85ec-142">Чтобы получить объект COMPUTE Node, используйте командлет Get-AzBatchComputeNode.</span><span class="sxs-lookup"><span data-stu-id="d85ec-142">To obtain a compute node object, use the Get-AzBatchComputeNode cmdlet.</span></span>

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

### <span data-ttu-id="d85ec-143">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="d85ec-143">-ComputeNodeId</span></span>
<span data-ttu-id="d85ec-144">Указывает идентификатор вычислительного узла, содержащего файлы командного узла.</span><span class="sxs-lookup"><span data-stu-id="d85ec-144">Specifies the ID of the compute node that contains the Batch node files.</span></span>

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

### <span data-ttu-id="d85ec-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d85ec-145">-DefaultProfile</span></span>
<span data-ttu-id="d85ec-146">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d85ec-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d85ec-147">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="d85ec-147">-Filter</span></span>
<span data-ttu-id="d85ec-148">Задает предложение фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="d85ec-148">Specifies an OData filter clause.</span></span>
<span data-ttu-id="d85ec-149">Этот командлет возвращает свойства для файлов узлов, соответствующих фильтру, указанному в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="d85ec-149">This cmdlet returns properties for node files that match the filter that this parameter specifies.</span></span>

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

### <span data-ttu-id="d85ec-150">-JobId</span><span class="sxs-lookup"><span data-stu-id="d85ec-150">-JobId</span></span>
<span data-ttu-id="d85ec-151">Указывает идентификатор задания, содержащего целевую задачу.</span><span class="sxs-lookup"><span data-stu-id="d85ec-151">Specifies the ID of the job that contains the target task.</span></span>

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

### <span data-ttu-id="d85ec-152">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="d85ec-152">-MaxCount</span></span>
<span data-ttu-id="d85ec-153">Указывает максимальное количество файлов узла, для которых этот командлет возвращает свойства.</span><span class="sxs-lookup"><span data-stu-id="d85ec-153">Specifies the maximum number of node files for which this cmdlet returns properties.</span></span>
<span data-ttu-id="d85ec-154">Если вы задаете нулевое значение (0) или меньше, в командлете не используется верхний предел.</span><span class="sxs-lookup"><span data-stu-id="d85ec-154">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="d85ec-155">Значение по умолчанию — 1000.</span><span class="sxs-lookup"><span data-stu-id="d85ec-155">The default value is 1000.</span></span>

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

### <span data-ttu-id="d85ec-156">-Path</span><span class="sxs-lookup"><span data-stu-id="d85ec-156">-Path</span></span>
<span data-ttu-id="d85ec-157">Задает путь к файлу узла, для которого этот командлет извлекает свойства.</span><span class="sxs-lookup"><span data-stu-id="d85ec-157">Specifies the path of the node file for which this cmdlet retrieves properties.</span></span>
<span data-ttu-id="d85ec-158">Подстановочные знаки указывать нельзя.</span><span class="sxs-lookup"><span data-stu-id="d85ec-158">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="d85ec-159">-PoolId</span><span class="sxs-lookup"><span data-stu-id="d85ec-159">-PoolId</span></span>
<span data-ttu-id="d85ec-160">Указывает идентификатор пула, который содержит вычислительный узел, из которого нужно получить свойства файлов узла.</span><span class="sxs-lookup"><span data-stu-id="d85ec-160">Specifies the ID of the pool that contains the compute node from which to get properties of node files.</span></span>

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

### <span data-ttu-id="d85ec-161">-Recursive</span><span class="sxs-lookup"><span data-stu-id="d85ec-161">-Recursive</span></span>
<span data-ttu-id="d85ec-162">Указывает на то, что этот командлет возвращает рекурсивный список файлов.</span><span class="sxs-lookup"><span data-stu-id="d85ec-162">Indicates that this cmdlet returns a recursive list of files.</span></span>
<span data-ttu-id="d85ec-163">В противном случае возвращаются только файлы в корневой папке.</span><span class="sxs-lookup"><span data-stu-id="d85ec-163">Otherwise, it returns only the files in the root folder.</span></span>

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

### <span data-ttu-id="d85ec-164">-Задача</span><span class="sxs-lookup"><span data-stu-id="d85ec-164">-Task</span></span>
<span data-ttu-id="d85ec-165">Указывает задачу как объект **PSCloudTask** , с которым связаны файлы узла.</span><span class="sxs-lookup"><span data-stu-id="d85ec-165">Specifies the task, as a **PSCloudTask** object, with which the node files are associated.</span></span>
<span data-ttu-id="d85ec-166">Чтобы получить объект Task, используйте командлет Get-AzBatchTask.</span><span class="sxs-lookup"><span data-stu-id="d85ec-166">To obtain a task object, use the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="d85ec-167">-TaskId</span><span class="sxs-lookup"><span data-stu-id="d85ec-167">-TaskId</span></span>
<span data-ttu-id="d85ec-168">Указывает идентификатор задачи, для которой этот командлет получает свойства файлов узла.</span><span class="sxs-lookup"><span data-stu-id="d85ec-168">Specifies the ID of the task for which this cmdlet gets properties of node files.</span></span>

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

### <span data-ttu-id="d85ec-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d85ec-169">CommonParameters</span></span>
<span data-ttu-id="d85ec-170">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d85ec-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d85ec-171">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d85ec-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d85ec-172">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d85ec-172">INPUTS</span></span>

### <span data-ttu-id="d85ec-173">System. String</span><span class="sxs-lookup"><span data-stu-id="d85ec-173">System.String</span></span>

### <span data-ttu-id="d85ec-174">Microsoft.Azure.Commands.BatCH. Models. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="d85ec-174">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="d85ec-175">Microsoft.Azure.Commands.BatCH. Models. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="d85ec-175">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="d85ec-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d85ec-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="d85ec-177">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d85ec-177">OUTPUTS</span></span>

### <span data-ttu-id="d85ec-178">Microsoft.Azure.Commands.BatCH. Models. PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="d85ec-178">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>

## <span data-ttu-id="d85ec-179">Пуск</span><span class="sxs-lookup"><span data-stu-id="d85ec-179">NOTES</span></span>

## <span data-ttu-id="d85ec-180">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d85ec-180">RELATED LINKS</span></span>

[<span data-ttu-id="d85ec-181">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="d85ec-181">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="d85ec-182">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="d85ec-182">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="d85ec-183">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="d85ec-183">Get-AzBatchNodeFileContent</span></span>](./Get-AzBatchNodeFileContent.md)

[<span data-ttu-id="d85ec-184">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="d85ec-184">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="d85ec-185">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="d85ec-185">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


