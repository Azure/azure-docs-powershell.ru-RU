---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C9E2D9EC-3B6A-492D-B183-9856185548CD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchnodefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFileContent.md
ms.openlocfilehash: 7795182ff1594c098a2afd778c137c48dc74c955
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566232"
---
# <span data-ttu-id="d3caa-101">Get-AzureBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="d3caa-101">Get-AzureBatchNodeFileContent</span></span>

## <span data-ttu-id="d3caa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d3caa-102">SYNOPSIS</span></span>
<span data-ttu-id="d3caa-103">Получает пакетный файл узла.</span><span class="sxs-lookup"><span data-stu-id="d3caa-103">Gets a Batch node file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3caa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d3caa-104">SYNTAX</span></span>

### <span data-ttu-id="d3caa-105">Task_Id_Path</span><span class="sxs-lookup"><span data-stu-id="d3caa-105">Task_Id_Path</span></span>
```
Get-AzureBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationPath <String>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3caa-106">Task_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="d3caa-106">Task_Id_Stream</span></span>
```
Get-AzureBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3caa-107">ComputeNode_Id_Path</span><span class="sxs-lookup"><span data-stu-id="d3caa-107">ComputeNode_Id_Path</span></span>
```
Get-AzureBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationPath <String> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3caa-108">ComputeNode_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="d3caa-108">ComputeNode_Id_Stream</span></span>
```
Get-AzureBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationStream <Stream> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3caa-109">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="d3caa-109">InputObject_Path</span></span>
```
Get-AzureBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationPath <String> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d3caa-110">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="d3caa-110">InputObject_Stream</span></span>
```
Get-AzureBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3caa-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3caa-111">DESCRIPTION</span></span>
<span data-ttu-id="d3caa-112">Командлет **Get-AzureBatchNodeFileContent** получает файл узла пакета Azure и сохраняет его в виде файла или потока.</span><span class="sxs-lookup"><span data-stu-id="d3caa-112">The **Get-AzureBatchNodeFileContent** cmdlet gets an Azure Batch node file and saves it as a file or to a stream.</span></span>

## <span data-ttu-id="d3caa-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d3caa-113">EXAMPLES</span></span>

### <span data-ttu-id="d3caa-114">Пример 1: получение файла узла пакета, связанного с задачей, и сохранение файла</span><span class="sxs-lookup"><span data-stu-id="d3caa-114">Example 1: Get a Batch node file associated with a task and save the file</span></span>
```
PS C:\>Get-AzureBatchNodeFileContent -JobId "Job01" -TaskId "Task01" -Path "StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="d3caa-115">Эта команда получает файл узла с именем StdOut.txt и сохраняет его в E:\PowerShell\StdOut.txt пути к файлу на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="d3caa-115">This command gets the node file that is named StdOut.txt, and saves it to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="d3caa-116">Файл узла StdOut.txt связан с задачей, которая имеет идентификатор Task01 для задания с ИД Job01.</span><span class="sxs-lookup"><span data-stu-id="d3caa-116">The StdOut.txt node file is associated with task that has the ID Task01 for the job that has the ID Job01.</span></span>
<span data-ttu-id="d3caa-117">Используйте командлет Get-AzureRmBatchAccountKeys для присвоения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="d3caa-117">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="d3caa-118">Пример 2: получение файла узла пакета и сохранение его по указанному пути с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="d3caa-118">Example 2: Get a Batch node file and save it to a specified file path using the pipeline</span></span>
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job02" -TaskId "Task02" -Path "StdErr.txt" -BatchContext $Context | Get-AzureBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="d3caa-119">Эта команда получает файл узла с именем StdErr.txt с помощью командлета Get-AzureBatchNodeFile.</span><span class="sxs-lookup"><span data-stu-id="d3caa-119">This command gets the node file that is named StdErr.txt by using the Get-AzureBatchNodeFile cmdlet.</span></span>
<span data-ttu-id="d3caa-120">Команда передает этот файл текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="d3caa-120">The command passes that file to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d3caa-121">Текущий командлет сохраняет этот файл в E:\PowerShell\StdOut.txt путь к файлу на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="d3caa-121">The current cmdlet saves that file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="d3caa-122">Файл узла StdOut.txt связан с задачей, которая имеет идентификатор Task02 для задания с ИД Job02.</span><span class="sxs-lookup"><span data-stu-id="d3caa-122">The StdOut.txt node file is associated with the task that has the ID Task02 for the job that has the ID Job02.</span></span>

### <span data-ttu-id="d3caa-123">Пример 3: получение файла узла пакета, связанного с задачей, и его направление в поток</span><span class="sxs-lookup"><span data-stu-id="d3caa-123">Example 3: Get a Batch node file associated with a task and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzureBatchNodeFileContent -JobId "Job03" -TaskId "Task11" -Path "StdOut.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="d3caa-124">Первая команда создает поток с помощью командлета New-Object и сохраняет его в переменной $Stream.</span><span class="sxs-lookup"><span data-stu-id="d3caa-124">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>

<span data-ttu-id="d3caa-125">Вторая команда получает файл узла с именем StdOut.txt из задачи с ИД Task11 для задания с ИД Job03.</span><span class="sxs-lookup"><span data-stu-id="d3caa-125">The second command gets the node file that is named StdOut.txt from the task that has the ID Task11 for the job that has the ID Job03.</span></span>
<span data-ttu-id="d3caa-126">Команда направляет содержимое файла в поток в $Stream.</span><span class="sxs-lookup"><span data-stu-id="d3caa-126">The command directs file contents to the stream in $Stream.</span></span>

### <span data-ttu-id="d3caa-127">Пример 4: получение файла узла на основе вычислительного узла и его сохранение</span><span class="sxs-lookup"><span data-stu-id="d3caa-127">Example 4: Get a node file from a compute node and save it</span></span>
```
PS C:\>Get-AzureBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="d3caa-128">Эта команда получает файл узла Startup\StdOut.txt из COMPUTE Node, который имеет ИД ComputeNode01 в пуле с ИД Pool01.</span><span class="sxs-lookup"><span data-stu-id="d3caa-128">This command gets the node file Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="d3caa-129">Команда сохраняет файл в E:\PowerShell\StdOut.txt путь к файлу на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="d3caa-129">The command saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="d3caa-130">Пример 5: получение файла узла на основе вычислительного узла и его сохранение с использованием конвейера</span><span class="sxs-lookup"><span data-stu-id="d3caa-130">Example 5: Get a node file from a compute node and save it by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchNodeFile -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context | Get-AzureBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="d3caa-131">Эта команда получает файл узла Startup\StdOut.txt с помощью Get-AzureBatchNodeFile из COMPUTE Node, у которого есть идентификатор ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="d3caa-131">This command gets the node file Startup\StdOut.txt by using Get-AzureBatchNodeFile from the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="d3caa-132">Вычислительный узел находится в пуле с ИДЕНТИФИКАТОРом Pool01.</span><span class="sxs-lookup"><span data-stu-id="d3caa-132">The compute node is in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="d3caa-133">Команда передает этот файл узла в текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="d3caa-133">The command passes that node file to the current cmdlet.</span></span>
<span data-ttu-id="d3caa-134">Этот командлет сохраняет файл в E:\PowerShell\StdOut.txt путь к файлу на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="d3caa-134">That cmdlet saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="d3caa-135">Пример 6: получение файла узла из вычислительного узла и его направление в поток</span><span class="sxs-lookup"><span data-stu-id="d3caa-135">Example 6: Get a node file from a compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzureBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "startup\stdout.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="d3caa-136">Первая команда создает поток с помощью командлета New-Object и сохраняет его в переменной $Stream.</span><span class="sxs-lookup"><span data-stu-id="d3caa-136">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>

<span data-ttu-id="d3caa-137">Вторая команда получает файл узла с именем StdOut.txt из COMPUTE Node, который имеет идентификатор ComputeNode01 в пуле с ИД Pool01.</span><span class="sxs-lookup"><span data-stu-id="d3caa-137">The second command gets the node file that is named StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="d3caa-138">Команда направляет содержимое файла в поток в $Stream.</span><span class="sxs-lookup"><span data-stu-id="d3caa-138">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="d3caa-139">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d3caa-139">PARAMETERS</span></span>

### <span data-ttu-id="d3caa-140">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d3caa-140">-BatchContext</span></span>
<span data-ttu-id="d3caa-141">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="d3caa-141">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d3caa-142">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="d3caa-142">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="d3caa-143">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="d3caa-143">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="d3caa-144">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="d3caa-144">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="d3caa-145">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="d3caa-145">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="d3caa-146">-ByteRangeEnd</span><span class="sxs-lookup"><span data-stu-id="d3caa-146">-ByteRangeEnd</span></span>
<span data-ttu-id="d3caa-147">Конец диапазона байтов для скачивания.</span><span class="sxs-lookup"><span data-stu-id="d3caa-147">The end of the byte range to be downloaded.</span></span>
```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3caa-148">-ByteRangeStart</span><span class="sxs-lookup"><span data-stu-id="d3caa-148">-ByteRangeStart</span></span>
<span data-ttu-id="d3caa-149">Начало диапазона байтов для загрузки.</span><span class="sxs-lookup"><span data-stu-id="d3caa-149">The start of the byte range to be downloaded.</span></span>
```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3caa-150">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="d3caa-150">-ComputeNodeId</span></span>
<span data-ttu-id="d3caa-151">Указывает идентификатор вычислительного узла, содержащего файл узла, возвращаемый этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="d3caa-151">Specifies the ID of the compute node that contains the node file that this cmdlet returns.</span></span>

```yaml
Type: String
Parameter Sets: ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3caa-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3caa-152">-DefaultProfile</span></span>
<span data-ttu-id="d3caa-153">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d3caa-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3caa-154">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="d3caa-154">-DestinationPath</span></span>
<span data-ttu-id="d3caa-155">Указывает путь к файлу, в котором командлет сохраняет файл узла.</span><span class="sxs-lookup"><span data-stu-id="d3caa-155">Specifies the file path where this cmdlet saves the node file.</span></span>

```yaml
Type: String
Parameter Sets: Task_Id_Path, ComputeNode_Id_Path, InputObject_Path
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3caa-156">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="d3caa-156">-DestinationStream</span></span>
<span data-ttu-id="d3caa-157">Указывает поток, в который этот командлет записывает содержимое файла узла.</span><span class="sxs-lookup"><span data-stu-id="d3caa-157">Specifies the stream into which this cmdlet writes the node file contents.</span></span>
<span data-ttu-id="d3caa-158">Этот командлет не закрывает и не перематывает этот поток.</span><span class="sxs-lookup"><span data-stu-id="d3caa-158">This cmdlet does not close or rewind this stream.</span></span>

```yaml
Type: Stream
Parameter Sets: Task_Id_Stream, ComputeNode_Id_Stream, InputObject_Stream
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3caa-159">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3caa-159">-InputObject</span></span>
<span data-ttu-id="d3caa-160">Указывает файл, который получает этот командлет, как объект **PSNodeFile** .</span><span class="sxs-lookup"><span data-stu-id="d3caa-160">Specifies the file that this cmdlet gets, as a **PSNodeFile** object.</span></span>
<span data-ttu-id="d3caa-161">Чтобы получить объект файла узла, используйте командлет Get-AzureBatchNodeFile.</span><span class="sxs-lookup"><span data-stu-id="d3caa-161">To obtain a node file object, use the Get-AzureBatchNodeFile cmdlet.</span></span>

```yaml
Type: PSNodeFile
Parameter Sets: InputObject_Path, InputObject_Stream
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3caa-162">-JobId</span><span class="sxs-lookup"><span data-stu-id="d3caa-162">-JobId</span></span>
<span data-ttu-id="d3caa-163">Указывает идентификатор задания, содержащего целевую задачу.</span><span class="sxs-lookup"><span data-stu-id="d3caa-163">Specifies the ID of the job that contains the target task.</span></span>

```yaml
Type: String
Parameter Sets: Task_Id_Path, Task_Id_Stream
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3caa-164">-Path</span><span class="sxs-lookup"><span data-stu-id="d3caa-164">-Path</span></span>
<span data-ttu-id="d3caa-165">Путь к файлу узла для скачивания.</span><span class="sxs-lookup"><span data-stu-id="d3caa-165">The path of the node file to download.</span></span>

```yaml
Type: String
Parameter Sets: Task_Id_Path, Task_Id_Stream, ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3caa-166">-PoolId</span><span class="sxs-lookup"><span data-stu-id="d3caa-166">-PoolId</span></span>
<span data-ttu-id="d3caa-167">Указывает идентификатор пула, который содержит вычислительный узел, содержащий файл узла, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d3caa-167">Specifies the ID of the pool that contains the compute node that contains the node file that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3caa-168">-TaskId</span><span class="sxs-lookup"><span data-stu-id="d3caa-168">-TaskId</span></span>
<span data-ttu-id="d3caa-169">Указывает идентификатор задачи.</span><span class="sxs-lookup"><span data-stu-id="d3caa-169">Specifies the ID of the task.</span></span>

```yaml
Type: String
Parameter Sets: Task_Id_Path, Task_Id_Stream
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3caa-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3caa-170">CommonParameters</span></span>
<span data-ttu-id="d3caa-171">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d3caa-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3caa-172">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3caa-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3caa-173">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d3caa-173">INPUTS</span></span>

### <span data-ttu-id="d3caa-174">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d3caa-174">BatchAccountContext</span></span>
<span data-ttu-id="d3caa-175">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="d3caa-175">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="d3caa-176">PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="d3caa-176">PSNodeFile</span></span>
<span data-ttu-id="d3caa-177">Параметр "InputObject" принимает значение типа "PSNodeFile" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="d3caa-177">Parameter 'InputObject' accepts value of type 'PSNodeFile' from the pipeline</span></span>

## <span data-ttu-id="d3caa-178">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3caa-178">OUTPUTS</span></span>

## <span data-ttu-id="d3caa-179">Пуск</span><span class="sxs-lookup"><span data-stu-id="d3caa-179">NOTES</span></span>

## <span data-ttu-id="d3caa-180">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d3caa-180">RELATED LINKS</span></span>

[<span data-ttu-id="d3caa-181">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="d3caa-181">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="d3caa-182">Get-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="d3caa-182">Get-AzureBatchNodeFile</span></span>](./Get-AzureBatchNodeFile.md)

[<span data-ttu-id="d3caa-183">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="d3caa-183">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


