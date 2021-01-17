---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C9E2D9EC-3B6A-492D-B183-9856185548CD
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchnodefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFileContent.md
ms.openlocfilehash: 534919a404ad415963408816b78e9bbf1f349965
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396967"
---
# <span data-ttu-id="930e0-101">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="930e0-101">Get-AzBatchNodeFileContent</span></span>

## <span data-ttu-id="930e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="930e0-102">SYNOPSIS</span></span>
<span data-ttu-id="930e0-103">Получает пакетный файл узла.</span><span class="sxs-lookup"><span data-stu-id="930e0-103">Gets a Batch node file.</span></span>

## <span data-ttu-id="930e0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="930e0-104">SYNTAX</span></span>

### <span data-ttu-id="930e0-105">Task_Id_Path</span><span class="sxs-lookup"><span data-stu-id="930e0-105">Task_Id_Path</span></span>
```
Get-AzBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationPath <String>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="930e0-106">Task_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="930e0-106">Task_Id_Stream</span></span>
```
Get-AzBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="930e0-107">ComputeNode_Id_Path</span><span class="sxs-lookup"><span data-stu-id="930e0-107">ComputeNode_Id_Path</span></span>
```
Get-AzBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationPath <String> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="930e0-108">ComputeNode_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="930e0-108">ComputeNode_Id_Stream</span></span>
```
Get-AzBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationStream <Stream> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="930e0-109">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="930e0-109">InputObject_Path</span></span>
```
Get-AzBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationPath <String> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="930e0-110">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="930e0-110">InputObject_Stream</span></span>
```
Get-AzBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationStream <Stream> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="930e0-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="930e0-111">DESCRIPTION</span></span>
<span data-ttu-id="930e0-112">Cmdlet **Get-AzBatchNodeFileContent** получает пакетный файл узла Azure и сохраняет его как файл или поток.</span><span class="sxs-lookup"><span data-stu-id="930e0-112">The **Get-AzBatchNodeFileContent** cmdlet gets an Azure Batch node file and saves it as a file or to a stream.</span></span>

## <span data-ttu-id="930e0-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="930e0-113">EXAMPLES</span></span>

### <span data-ttu-id="930e0-114">Пример 1. Получите пакетный файл узла, связанный с задачей, и сохраните его</span><span class="sxs-lookup"><span data-stu-id="930e0-114">Example 1: Get a Batch node file associated with a task and save the file</span></span>
```
PS C:\>Get-AzBatchNodeFileContent -JobId "Job01" -TaskId "Task01" -Path "StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="930e0-115">Эта команда получает файл узла с именем StdOut.txt и сохраняет его в E:\PowerShell\StdOut.txt пути на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="930e0-115">This command gets the node file that is named StdOut.txt, and saves it to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="930e0-116">Файл StdOut.txt связан с задачей, которая имеет задачу "ID Task01" для задания, которое имеет задание "ИД01".</span><span class="sxs-lookup"><span data-stu-id="930e0-116">The StdOut.txt node file is associated with task that has the ID Task01 for the job that has the ID Job01.</span></span>
<span data-ttu-id="930e0-117">Используйте Get-AzBatchAccountKey для назначения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="930e0-117">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="930e0-118">Пример 2. Получите пакетный файл узла и сохраните его в заданный путь к файлу с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="930e0-118">Example 2: Get a Batch node file and save it to a specified file path using the pipeline</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job02" -TaskId "Task02" -Path "StdErr.txt" -BatchContext $Context | Get-AzBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="930e0-119">Эта команда получает файл узла с именем "StdErr.txt с помощью Get-AzBatchNodeFile командлета.</span><span class="sxs-lookup"><span data-stu-id="930e0-119">This command gets the node file that is named StdErr.txt by using the Get-AzBatchNodeFile cmdlet.</span></span>
<span data-ttu-id="930e0-120">Эта команда передает этот файл текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="930e0-120">The command passes that file to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="930e0-121">Текущий cmdlet сохраняет этот файл в E:\PowerShell\StdOut.txt путь к файлу на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="930e0-121">The current cmdlet saves that file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="930e0-122">Файл StdOut.txt связан с задачей, которая имеет задачу "ID Task02" для задания, которое имеет задание "ИД02".</span><span class="sxs-lookup"><span data-stu-id="930e0-122">The StdOut.txt node file is associated with the task that has the ID Task02 for the job that has the ID Job02.</span></span>

### <span data-ttu-id="930e0-123">Пример 3. Получить пакетный файл узла, связанный с задачей, и направить его к потоку</span><span class="sxs-lookup"><span data-stu-id="930e0-123">Example 3: Get a Batch node file associated with a task and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchNodeFileContent -JobId "Job03" -TaskId "Task11" -Path "StdOut.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="930e0-124">Первая команда создает поток с помощью New-Object командлета, а затем сохраняет его в $Stream переменной.</span><span class="sxs-lookup"><span data-stu-id="930e0-124">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="930e0-125">Вторая команда получает файл узла, который называется StdOut.txt из задачи, которая имеет задачу "ИД11" для задания, для которого назначено задание "ИД03".</span><span class="sxs-lookup"><span data-stu-id="930e0-125">The second command gets the node file that is named StdOut.txt from the task that has the ID Task11 for the job that has the ID Job03.</span></span>
<span data-ttu-id="930e0-126">Команда направляет содержимое файла в поток в $Stream.</span><span class="sxs-lookup"><span data-stu-id="930e0-126">The command directs file contents to the stream in $Stream.</span></span>

### <span data-ttu-id="930e0-127">Пример 4. Получите файл узла из узла вычислений и сохраните его</span><span class="sxs-lookup"><span data-stu-id="930e0-127">Example 4: Get a node file from a compute node and save it</span></span>
```
PS C:\>Get-AzBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="930e0-128">Эта команда получает файл узла Startup\StdOut.txt из узла вычислений, который имеет ID ComputeNode01 в пуле, который содержит пул ID Pool01.</span><span class="sxs-lookup"><span data-stu-id="930e0-128">This command gets the node file Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="930e0-129">Команда сохраняет файл в папкуE:\PowerShell\StdOut.txt путь к файлу на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="930e0-129">The command saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="930e0-130">Пример 5. Получите файл узла из узла вычислений и сохраните его с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="930e0-130">Example 5: Get a node file from a compute node and save it by using the pipeline</span></span>
```
PS C:\>Get-AzBatchNodeFile -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context | Get-AzBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="930e0-131">Эта команда получает файл узла Startup\StdOut.txt с помощью Get-AzBatchNodeFile узла вычислений, который имеет ID ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="930e0-131">This command gets the node file Startup\StdOut.txt by using Get-AzBatchNodeFile from the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="930e0-132">Узел вычислений находится в пуле с пулом ID Pool01.</span><span class="sxs-lookup"><span data-stu-id="930e0-132">The compute node is in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="930e0-133">Эта команда передает этот файл узла текущему командлету.</span><span class="sxs-lookup"><span data-stu-id="930e0-133">The command passes that node file to the current cmdlet.</span></span>
<span data-ttu-id="930e0-134">Этот cmdlet сохраняет файл в E:\PowerShell\StdOut.txt путь к файлу на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="930e0-134">That cmdlet saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="930e0-135">Пример 6. Получить файл узла из узла вычислений и направить его в поток</span><span class="sxs-lookup"><span data-stu-id="930e0-135">Example 6: Get a node file from a compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "startup\stdout.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="930e0-136">Первая команда создает поток с помощью New-Object командлета, а затем сохраняет его в $Stream переменной.</span><span class="sxs-lookup"><span data-stu-id="930e0-136">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="930e0-137">Вторая команда получает файл узла с именем StdOut.txt узла вычислений, в пуле которого есть ID ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="930e0-137">The second command gets the node file that is named StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="930e0-138">Команда направляет содержимое файла в поток в $Stream.</span><span class="sxs-lookup"><span data-stu-id="930e0-138">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="930e0-139">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="930e0-139">PARAMETERS</span></span>

### <span data-ttu-id="930e0-140">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="930e0-140">-BatchContext</span></span>
<span data-ttu-id="930e0-141">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="930e0-141">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="930e0-142">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой пакета будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="930e0-142">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="930e0-143">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="930e0-143">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="930e0-144">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="930e0-144">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="930e0-145">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="930e0-145">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="930e0-146">-ByteRangeEnd</span><span class="sxs-lookup"><span data-stu-id="930e0-146">-ByteRangeEnd</span></span>
<span data-ttu-id="930e0-147">Конец загружаемого диапазона byte.</span><span class="sxs-lookup"><span data-stu-id="930e0-147">The end of the byte range to be downloaded.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="930e0-148">-ByteRangeStart</span><span class="sxs-lookup"><span data-stu-id="930e0-148">-ByteRangeStart</span></span>
<span data-ttu-id="930e0-149">Начало загружаемого диапазона byte.</span><span class="sxs-lookup"><span data-stu-id="930e0-149">The start of the byte range to be downloaded.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="930e0-150">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="930e0-150">-ComputeNodeId</span></span>
<span data-ttu-id="930e0-151">Определяет код узла вычислений, содержаного файл узла, который возвращает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="930e0-151">Specifies the ID of the compute node that contains the node file that this cmdlet returns.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="930e0-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="930e0-152">-DefaultProfile</span></span>
<span data-ttu-id="930e0-153">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="930e0-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="930e0-154">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="930e0-154">-DestinationPath</span></span>
<span data-ttu-id="930e0-155">Путь к файлу, в котором этот cmdlet сохраняет файл узла.</span><span class="sxs-lookup"><span data-stu-id="930e0-155">Specifies the file path where this cmdlet saves the node file.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, ComputeNode_Id_Path, InputObject_Path
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="930e0-156">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="930e0-156">-DestinationStream</span></span>
<span data-ttu-id="930e0-157">Определяет поток, в который этот cmdlet записывает содержимое файла узла.</span><span class="sxs-lookup"><span data-stu-id="930e0-157">Specifies the stream into which this cmdlet writes the node file contents.</span></span>
<span data-ttu-id="930e0-158">Этот cmdlet не закрывает и не перемотать этот поток.</span><span class="sxs-lookup"><span data-stu-id="930e0-158">This cmdlet does not close or rewind this stream.</span></span>

```yaml
Type: System.IO.Stream
Parameter Sets: Task_Id_Stream, ComputeNode_Id_Stream, InputObject_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="930e0-159">-InputObject</span><span class="sxs-lookup"><span data-stu-id="930e0-159">-InputObject</span></span>
<span data-ttu-id="930e0-160">Определяет файл, который получает этот cmdlet как объект **PSNodeFile.**</span><span class="sxs-lookup"><span data-stu-id="930e0-160">Specifies the file that this cmdlet gets, as a **PSNodeFile** object.</span></span>
<span data-ttu-id="930e0-161">Чтобы получить объект в файле узла, используйте Get-AzBatchNodeFile-файл.</span><span class="sxs-lookup"><span data-stu-id="930e0-161">To obtain a node file object, use the Get-AzBatchNodeFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSNodeFile
Parameter Sets: InputObject_Path, InputObject_Stream
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="930e0-162">-JobId</span><span class="sxs-lookup"><span data-stu-id="930e0-162">-JobId</span></span>
<span data-ttu-id="930e0-163">Определяет ИД задания, которое содержит целевую задачу.</span><span class="sxs-lookup"><span data-stu-id="930e0-163">Specifies the ID of the job that contains the target task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="930e0-164">-Path</span><span class="sxs-lookup"><span data-stu-id="930e0-164">-Path</span></span>
<span data-ttu-id="930e0-165">Путь к файлу узла, который нужно скачать.</span><span class="sxs-lookup"><span data-stu-id="930e0-165">The path of the node file to download.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream, ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="930e0-166">-PoolId</span><span class="sxs-lookup"><span data-stu-id="930e0-166">-PoolId</span></span>
<span data-ttu-id="930e0-167">Определяет код пула, который содержит узел вычислений, содержащий файл узла, который получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="930e0-167">Specifies the ID of the pool that contains the compute node that contains the node file that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="930e0-168">-TaskId</span><span class="sxs-lookup"><span data-stu-id="930e0-168">-TaskId</span></span>
<span data-ttu-id="930e0-169">Определяет ИД задачи.</span><span class="sxs-lookup"><span data-stu-id="930e0-169">Specifies the ID of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="930e0-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="930e0-170">CommonParameters</span></span>
<span data-ttu-id="930e0-171">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="930e0-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="930e0-172">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="930e0-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="930e0-173">INPUTS</span><span class="sxs-lookup"><span data-stu-id="930e0-173">INPUTS</span></span>

### <span data-ttu-id="930e0-174">System.String</span><span class="sxs-lookup"><span data-stu-id="930e0-174">System.String</span></span>

### <span data-ttu-id="930e0-175">Microsoft.Azure.Commands.Batch. Models.PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="930e0-175">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>

### <span data-ttu-id="930e0-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="930e0-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="930e0-177">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="930e0-177">OUTPUTS</span></span>

### <span data-ttu-id="930e0-178">System.Void</span><span class="sxs-lookup"><span data-stu-id="930e0-178">System.Void</span></span>

## <span data-ttu-id="930e0-179">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="930e0-179">NOTES</span></span>

## <span data-ttu-id="930e0-180">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="930e0-180">RELATED LINKS</span></span>

[<span data-ttu-id="930e0-181">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="930e0-181">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="930e0-182">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="930e0-182">Get-AzBatchNodeFile</span></span>](./Get-AzBatchNodeFile.md)

[<span data-ttu-id="930e0-183">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="930e0-183">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
