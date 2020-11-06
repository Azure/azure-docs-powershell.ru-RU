---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 38ED2854-23D0-400E-A5C8-239346B2AF99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchnodefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFile.md
ms.openlocfilehash: ac9a49b52dd2fecea12e3084e4d86077ddb06cb5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566233"
---
# <span data-ttu-id="b5a74-101">Get-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="b5a74-101">Get-AzureBatchNodeFile</span></span>

## <span data-ttu-id="b5a74-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b5a74-102">SYNOPSIS</span></span>
<span data-ttu-id="b5a74-103">Возвращает свойства файлов узлов пакета.</span><span class="sxs-lookup"><span data-stu-id="b5a74-103">Gets the properties of Batch node files.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5a74-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b5a74-104">SYNTAX</span></span>

### <span data-ttu-id="b5a74-105">ComputeNode_Id (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b5a74-105">ComputeNode_Id (Default)</span></span>
```
Get-AzureBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> [[-Path] <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5a74-106">Task_Id</span><span class="sxs-lookup"><span data-stu-id="b5a74-106">Task_Id</span></span>
```
Get-AzureBatchNodeFile -JobId <String> -TaskId <String> [[-Path] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5a74-107">Task_ODataFilter</span><span class="sxs-lookup"><span data-stu-id="b5a74-107">Task_ODataFilter</span></span>
```
Get-AzureBatchNodeFile -JobId <String> -TaskId <String> [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5a74-108">ParentTask</span><span class="sxs-lookup"><span data-stu-id="b5a74-108">ParentTask</span></span>
```
Get-AzureBatchNodeFile [[-Task] <PSCloudTask>] [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5a74-109">ComputeNode_ODataFilter</span><span class="sxs-lookup"><span data-stu-id="b5a74-109">ComputeNode_ODataFilter</span></span>
```
Get-AzureBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Recursive] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b5a74-110">ParentComputeNode</span><span class="sxs-lookup"><span data-stu-id="b5a74-110">ParentComputeNode</span></span>
```
Get-AzureBatchNodeFile [[-ComputeNode] <PSComputeNode>] [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5a74-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5a74-111">DESCRIPTION</span></span>
<span data-ttu-id="b5a74-112">Командлет **Get-AzureBatchNodeFile** получает свойства файлов пакетных узлов Azure для задачи или вычислительного узла.</span><span class="sxs-lookup"><span data-stu-id="b5a74-112">The **Get-AzureBatchNodeFile** cmdlet gets the properties of the Azure Batch node files of a task or compute node.</span></span>
<span data-ttu-id="b5a74-113">Чтобы сузить результаты, вы можете указать фильтр протокола OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="b5a74-113">To narrow your results, you can specify an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="b5a74-114">Если вы укажете задачу, но не фильтр, этот командлет возвращает свойства для всех файлов узла для этой задачи.</span><span class="sxs-lookup"><span data-stu-id="b5a74-114">If you specify a task, but not a filter, this cmdlet returns properties for all node files for that task.</span></span>
<span data-ttu-id="b5a74-115">Если указать вычислительный узел, но не фильтр, этот командлет возвращает свойства для всех файлов узлов для этого вычислительного узла.</span><span class="sxs-lookup"><span data-stu-id="b5a74-115">If you specify a compute node, but not a filter, this cmdlet returns properties for all node files for that compute node.</span></span>

## <span data-ttu-id="b5a74-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b5a74-116">EXAMPLES</span></span>

### <span data-ttu-id="b5a74-117">Пример 1: получение свойств файла узла, связанного с задачей</span><span class="sxs-lookup"><span data-stu-id="b5a74-117">Example 1: Get the properties of a node file associated with a task</span></span>
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "Stdout.txt" -BatchContext $Context
IsDirectory Name          Properties                                      Url

----------- ----          ----------                                      ---

False       StdOut.txt    Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="b5a74-118">Эта команда получает свойства файла узла StdOut.txt, связанного с задачей, которая имеет идентификатор Task26 в задании с ИД задания 000001.</span><span class="sxs-lookup"><span data-stu-id="b5a74-118">This command gets the properties of the StdOut.txt node file associated with the task that has the ID Task26 in the job that has the ID Job-000001.</span></span>
<span data-ttu-id="b5a74-119">Используйте командлет Get-AzureRmBatchAccountKeys для присвоения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="b5a74-119">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="b5a74-120">Пример 2: получение свойств файлов узла, связанных с задачей с помощью фильтра</span><span class="sxs-lookup"><span data-stu-id="b5a74-120">Example 2: Get the properties of node files associated with a task by using a filter</span></span>
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job-00002" -TaskId "Task26" -Filter "startswith(name,'St')" -BatchContext $Context
IsDirectory Name        Properties                                      Url

----------- ----        ----------                                      ---

False       StdErr.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       StdOut.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="b5a74-121">Эта команда получает свойства файлов узла, имена которых начинаются с ST и связанные с задачей, которая имеет идентификатор Task26 в разделе Задание с ИД задания 00002.</span><span class="sxs-lookup"><span data-stu-id="b5a74-121">This command gets the properties of the node files whose names start with st and are associated with task that has the ID Task26 under job that has the ID Job-00002.</span></span>

### <span data-ttu-id="b5a74-122">Пример 3: рекурсивное получение свойств файлов узлов, связанных с задачей</span><span class="sxs-lookup"><span data-stu-id="b5a74-122">Example 3: Recursively get the properties of node files associated with a task</span></span>
```
PS C:\>Get-AzureBatchTask "Job-00003" "Task31" -BatchContext $Context | Get-AzureBatchNodeFile -Recursive -BatchContext $Context
IsDirectory Name             Properties                                      Url

----------- ----             ----------                                      ---

False       ProcessEnv.cmd   Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       StdErr.txt       Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       StdOut.txt       Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
True        wd                                                               https://cmdletexample.westus.Batch.contoso... 
False       wd\newFile.txt   Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="b5a74-123">Эта команда получает свойства всех файлов, связанных с задачей, которая имеет идентификатор Task31 в задании задания — 00003.</span><span class="sxs-lookup"><span data-stu-id="b5a74-123">This command gets the properties of all files associated with the task that has the ID Task31 in job Job-00003.</span></span>
<span data-ttu-id="b5a74-124">Эта команда задает *рекурсивный* параметр.</span><span class="sxs-lookup"><span data-stu-id="b5a74-124">This command specifies the *Recursive* parameter.</span></span>
<span data-ttu-id="b5a74-125">Таким образом, командлет выполняет рекурсивный поиск файла и возвращает файл узла wd\newFile.txt.</span><span class="sxs-lookup"><span data-stu-id="b5a74-125">Therefore, the cmdlet performs a recursive file search is performed, and returns the wd\newFile.txt node file.</span></span>

### <span data-ttu-id="b5a74-126">Пример 4: получение одного файла из вычислительного узла</span><span class="sxs-lookup"><span data-stu-id="b5a74-126">Example 4: Get a single file from a compute node</span></span>
```
PS C:\>Get-AzureBatchNodeFile -PoolId "Pool22" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context
IsDirectory Name                    Properties                                      Url
----------- ----                    ----------                                      ---
False       startup\stdout.txt      Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="b5a74-127">Эта команда получает файл с именем Startup\StdOut.txt из COMPUTE Node, который имеет идентификатор ComputeNode01 в пуле с ИД Pool22.</span><span class="sxs-lookup"><span data-stu-id="b5a74-127">This command gets the file that is named Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>

### <span data-ttu-id="b5a74-128">Пример 5: получение всех файлов в папке с помощью вычислительного узла</span><span class="sxs-lookup"><span data-stu-id="b5a74-128">Example 5: Get all files under a folder from a compute node</span></span>
```
PS C:\>Get-AzureBatchNodeFile -PoolId "Pool22" -ComputeNodeId "ComputeNode01" -Filter "startswith(name,'startup')" -Recursive -BatchContext $Context
IsDirectory Name                      Properties                                      Url
----------- ----                      ----------                                      ---
True        startup                                                                   https://cmdletexample.westus.Batch.contoso... 
False       startup\ProcessEnv.cmd    Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       startup\stderr.txt        Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       startup\stdout.txt        Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
True        startup\wd                                                                https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="b5a74-129">Эта команда получает все файлы в папке "Автозагрузка" с узла COMPUTE node с ИД ComputeNode01 в пуле с ИД Pool22.</span><span class="sxs-lookup"><span data-stu-id="b5a74-129">This command gets all the files under the startup folder from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>
<span data-ttu-id="b5a74-130">Этот командлет задает *рекурсивный* параметр.</span><span class="sxs-lookup"><span data-stu-id="b5a74-130">This cmdlet specifies the *Recursive* parameter.</span></span>

### <span data-ttu-id="b5a74-131">Пример 6: получение файлов из корневой папки вычислительного узла</span><span class="sxs-lookup"><span data-stu-id="b5a74-131">Example 6: Get files from the root folder of a compute node</span></span>
```
PS C:\>Get-AzureBatchComputeNode "Pool22" -Id "ComputeNode01" -BatchContext $Context | Get-AzureBatchNodeFile -BatchContext $Context
IsDirectory Name           Properties       Url
----------- ----           ----------       ---
True        shared                          https://cmdletexample.westus.Batch.contoso... 
True        startup                         https://cmdletexample.westus.Batch.contoso... 
True        workitems                       https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="b5a74-132">Эта команда получает все файлы в корневой папке вычислительного узла с ИД ComputeNode01 в пуле с ИД Pool22.</span><span class="sxs-lookup"><span data-stu-id="b5a74-132">This command gets all the files at the root folder of the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>

## <span data-ttu-id="b5a74-133">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b5a74-133">PARAMETERS</span></span>

### <span data-ttu-id="b5a74-134">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b5a74-134">-BatchContext</span></span>
<span data-ttu-id="b5a74-135">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="b5a74-135">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b5a74-136">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="b5a74-136">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b5a74-137">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="b5a74-137">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b5a74-138">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="b5a74-138">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b5a74-139">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="b5a74-139">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="b5a74-140">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="b5a74-140">-ComputeNode</span></span>
<span data-ttu-id="b5a74-141">Задает вычислительный узел как объект **PSComputeNode** , содержащий пакетные файлы узла.</span><span class="sxs-lookup"><span data-stu-id="b5a74-141">Specifies the compute node, as a **PSComputeNode** object, that contains the Batch node files.</span></span>
<span data-ttu-id="b5a74-142">Чтобы получить объект COMPUTE Node, используйте командлет Get-AzureBatchComputeNode.</span><span class="sxs-lookup"><span data-stu-id="b5a74-142">To obtain a compute node object, use the Get-AzureBatchComputeNode cmdlet.</span></span>

```yaml
Type: PSComputeNode
Parameter Sets: ParentComputeNode
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5a74-143">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="b5a74-143">-ComputeNodeId</span></span>
<span data-ttu-id="b5a74-144">Указывает идентификатор вычислительного узла, содержащего файлы командного узла.</span><span class="sxs-lookup"><span data-stu-id="b5a74-144">Specifies the ID of the compute node that contains the Batch node files.</span></span>

```yaml
Type: String
Parameter Sets: ComputeNode_Id, ComputeNode_ODataFilter
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5a74-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5a74-145">-DefaultProfile</span></span>
<span data-ttu-id="b5a74-146">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b5a74-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5a74-147">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="b5a74-147">-Filter</span></span>
<span data-ttu-id="b5a74-148">Задает предложение фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="b5a74-148">Specifies an OData filter clause.</span></span>
<span data-ttu-id="b5a74-149">Этот командлет возвращает свойства для файлов узлов, соответствующих фильтру, указанному в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="b5a74-149">This cmdlet returns properties for node files that match the filter that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Task_ODataFilter, ParentTask, ComputeNode_ODataFilter, ParentComputeNode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5a74-150">-JobId</span><span class="sxs-lookup"><span data-stu-id="b5a74-150">-JobId</span></span>
<span data-ttu-id="b5a74-151">Указывает идентификатор задания, содержащего целевую задачу.</span><span class="sxs-lookup"><span data-stu-id="b5a74-151">Specifies the ID of the job that contains the target task.</span></span>

```yaml
Type: String
Parameter Sets: Task_Id, Task_ODataFilter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5a74-152">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="b5a74-152">-MaxCount</span></span>
<span data-ttu-id="b5a74-153">Указывает максимальное количество файлов узла, для которых этот командлет возвращает свойства.</span><span class="sxs-lookup"><span data-stu-id="b5a74-153">Specifies the maximum number of node files for which this cmdlet returns properties.</span></span>
<span data-ttu-id="b5a74-154">Если вы задаете нулевое значение (0) или меньше, в командлете не используется верхний предел.</span><span class="sxs-lookup"><span data-stu-id="b5a74-154">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="b5a74-155">Значение по умолчанию — 1000.</span><span class="sxs-lookup"><span data-stu-id="b5a74-155">The default value is 1000.</span></span>

```yaml
Type: Int32
Parameter Sets: Task_ODataFilter, ParentTask, ComputeNode_ODataFilter, ParentComputeNode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5a74-156">-Path</span><span class="sxs-lookup"><span data-stu-id="b5a74-156">-Path</span></span>
<span data-ttu-id="b5a74-157">Задает путь к файлу узла, для которого этот командлет извлекает свойства.</span><span class="sxs-lookup"><span data-stu-id="b5a74-157">Specifies the path of the node file for which this cmdlet retrieves properties.</span></span>
<span data-ttu-id="b5a74-158">Подстановочные знаки указывать нельзя.</span><span class="sxs-lookup"><span data-stu-id="b5a74-158">You cannot specify wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: ComputeNode_Id, Task_Id
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5a74-159">-PoolId</span><span class="sxs-lookup"><span data-stu-id="b5a74-159">-PoolId</span></span>
<span data-ttu-id="b5a74-160">Указывает идентификатор пула, который содержит вычислительный узел, из которого нужно получить свойства файлов узла.</span><span class="sxs-lookup"><span data-stu-id="b5a74-160">Specifies the ID of the pool that contains the compute node from which to get properties of node files.</span></span>

```yaml
Type: String
Parameter Sets: ComputeNode_Id, ComputeNode_ODataFilter
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5a74-161">-Recursive</span><span class="sxs-lookup"><span data-stu-id="b5a74-161">-Recursive</span></span>
<span data-ttu-id="b5a74-162">Указывает на то, что этот командлет возвращает рекурсивный список файлов.</span><span class="sxs-lookup"><span data-stu-id="b5a74-162">Indicates that this cmdlet returns a recursive list of files.</span></span>
<span data-ttu-id="b5a74-163">В противном случае возвращаются только файлы в корневой папке.</span><span class="sxs-lookup"><span data-stu-id="b5a74-163">Otherwise, it returns only the files in the root folder.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Task_ODataFilter, ParentTask, ComputeNode_ODataFilter, ParentComputeNode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5a74-164">-Задача</span><span class="sxs-lookup"><span data-stu-id="b5a74-164">-Task</span></span>
<span data-ttu-id="b5a74-165">Указывает задачу как объект **PSCloudTask** , с которым связаны файлы узла.</span><span class="sxs-lookup"><span data-stu-id="b5a74-165">Specifies the task, as a **PSCloudTask** object, with which the node files are associated.</span></span>
<span data-ttu-id="b5a74-166">Чтобы получить объект Task, используйте командлет Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="b5a74-166">To obtain a task object, use the Get-AzureBatchTask cmdlet.</span></span>

```yaml
Type: PSCloudTask
Parameter Sets: ParentTask
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5a74-167">-TaskId</span><span class="sxs-lookup"><span data-stu-id="b5a74-167">-TaskId</span></span>
<span data-ttu-id="b5a74-168">Указывает идентификатор задачи, для которой этот командлет получает свойства файлов узла.</span><span class="sxs-lookup"><span data-stu-id="b5a74-168">Specifies the ID of the task for which this cmdlet gets properties of node files.</span></span>

```yaml
Type: String
Parameter Sets: Task_Id, Task_ODataFilter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5a74-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5a74-169">CommonParameters</span></span>
<span data-ttu-id="b5a74-170">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b5a74-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5a74-171">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5a74-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5a74-172">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b5a74-172">INPUTS</span></span>

### <span data-ttu-id="b5a74-173">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b5a74-173">BatchAccountContext</span></span>
<span data-ttu-id="b5a74-174">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="b5a74-174">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="b5a74-175">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="b5a74-175">PSComputeNode</span></span>
<span data-ttu-id="b5a74-176">Параметр "ComputeNode" принимает значение типа "PSComputeNode" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="b5a74-176">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

### <span data-ttu-id="b5a74-177">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="b5a74-177">PSCloudTask</span></span>
<span data-ttu-id="b5a74-178">Параметр "задача" принимает значение типа "PSCloudTask" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="b5a74-178">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="b5a74-179">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5a74-179">OUTPUTS</span></span>

### <span data-ttu-id="b5a74-180">PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="b5a74-180">PSNodeFile</span></span>

## <span data-ttu-id="b5a74-181">Пуск</span><span class="sxs-lookup"><span data-stu-id="b5a74-181">NOTES</span></span>

## <span data-ttu-id="b5a74-182">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b5a74-182">RELATED LINKS</span></span>

[<span data-ttu-id="b5a74-183">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="b5a74-183">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="b5a74-184">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="b5a74-184">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="b5a74-185">Get-AzureBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="b5a74-185">Get-AzureBatchNodeFileContent</span></span>](./Get-AzureBatchNodeFileContent.md)

[<span data-ttu-id="b5a74-186">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="b5a74-186">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="b5a74-187">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="b5a74-187">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


