---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: DBA02017-8372-4A91-A4F1-985777DEDAB9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchNodeFile.md
ms.openlocfilehash: 5b8797cf2f6068098d1ca407f0f97283dd171af5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565649"
---
# <span data-ttu-id="e992c-101">Remove-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="e992c-101">Remove-AzureBatchNodeFile</span></span>

## <span data-ttu-id="e992c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e992c-102">SYNOPSIS</span></span>
<span data-ttu-id="e992c-103">Удаляет файл узла для задачи или вычислительного узла.</span><span class="sxs-lookup"><span data-stu-id="e992c-103">Deletes a node file for a task or compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e992c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e992c-104">SYNTAX</span></span>

### <span data-ttu-id="e992c-105">Задачи</span><span class="sxs-lookup"><span data-stu-id="e992c-105">Task</span></span>
```
Remove-AzureBatchNodeFile -JobId <String> -TaskId <String> -Name <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e992c-106">ComputeNode</span><span class="sxs-lookup"><span data-stu-id="e992c-106">ComputeNode</span></span>
```
Remove-AzureBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> -Name <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e992c-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="e992c-107">InputObject</span></span>
```
Remove-AzureBatchNodeFile [[-InputObject] <PSNodeFile>] [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e992c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e992c-108">DESCRIPTION</span></span>
<span data-ttu-id="e992c-109">Командлет **Remove-AzureBatchNodeFile** удаляет пакетный файл узла Azure для задачи или вычислительного узла.</span><span class="sxs-lookup"><span data-stu-id="e992c-109">The **Remove-AzureBatchNodeFile** cmdlet deletes an Azure Batch node file for a task or compute node.</span></span>

## <span data-ttu-id="e992c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e992c-110">EXAMPLES</span></span>

### <span data-ttu-id="e992c-111">Пример 1: удаление файла, assocated с задачей</span><span class="sxs-lookup"><span data-stu-id="e992c-111">Example 1: Delete a file assocated with a task</span></span>
```
PS C:\>Remove-AzureBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Name "wd\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="e992c-112">Эта команда удаляет файл узла с именем wd\testFile.txt.</span><span class="sxs-lookup"><span data-stu-id="e992c-112">This command deletes the node file that is named wd\testFile.txt.</span></span>
<span data-ttu-id="e992c-113">Этот файл связан с задачей, которая имеет идентификатор Task26 под заданием задания — 000001.</span><span class="sxs-lookup"><span data-stu-id="e992c-113">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>

### <span data-ttu-id="e992c-114">Пример 2: удаление файла из вычислительного узла</span><span class="sxs-lookup"><span data-stu-id="e992c-114">Example 2: Delete a file from a compute node</span></span>
```
PS C:\>Remove-AzureBatchNodeFile -PoolId "Pool07" -ComputeNodeId "tvm-2316545714_1-20150725t213220z" -Name "startup\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="e992c-115">Эта команда удаляет файл узла с именем startup\testFile.txt из указанного вычислительного узла в пуле с ИДЕНТИФИКАТОРом Pool07.</span><span class="sxs-lookup"><span data-stu-id="e992c-115">This command deletes the node file that is named startup\testFile.txt from the specified compute node in the pool that has the ID Pool07.</span></span>

### <span data-ttu-id="e992c-116">Пример 3: удаление файла с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="e992c-116">Example 3: Remove a file by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Name "wd\testFile2.txt" -BatchContext $Context | Remove-AzureBatchNodeFile -Force -BatchContext $Context
```

<span data-ttu-id="e992c-117">Эта команда получает файл узла с помощью **Get-AzureBatchNodeFile**.</span><span class="sxs-lookup"><span data-stu-id="e992c-117">This command gets the node file by using **Get-AzureBatchNodeFile**.</span></span>
<span data-ttu-id="e992c-118">Этот файл связан с задачей, которая имеет идентификатор Task26 под заданием задания — 000001.</span><span class="sxs-lookup"><span data-stu-id="e992c-118">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>
<span data-ttu-id="e992c-119">Команда передает этот файл текущему командлету с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="e992c-119">The command passes that file to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="e992c-120">Текущий командлет удаляет файл узла.</span><span class="sxs-lookup"><span data-stu-id="e992c-120">The current cmdlet removes the node file.</span></span>
<span data-ttu-id="e992c-121">Команда задает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="e992c-121">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="e992c-122">Таким образом, команда не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="e992c-122">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="e992c-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e992c-123">PARAMETERS</span></span>

### <span data-ttu-id="e992c-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e992c-124">-BatchContext</span></span>
<span data-ttu-id="e992c-125">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="e992c-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e992c-126">Чтобы получить объект **BatchAccountContext** , содержащий клавиши доступа для вашей подписки, используйте командлет Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="e992c-126">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="e992c-127">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="e992c-127">-ComputeNodeId</span></span>
<span data-ttu-id="e992c-128">Указывает идентификатор вычислительного узла, содержащего файл узла пакета, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="e992c-128">Specifies the ID of the compute node that contains the Batch node file that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e992c-129">-Force</span><span class="sxs-lookup"><span data-stu-id="e992c-129">-Force</span></span>
<span data-ttu-id="e992c-130">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="e992c-130">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e992c-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e992c-131">-InputObject</span></span>
<span data-ttu-id="e992c-132">Указывает объект **PSNodeFile** , представляющий файл узла, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="e992c-132">Specifies **PSNodeFile** object that represent the node file that this cmdlet deletes.</span></span>
<span data-ttu-id="e992c-133">Чтобы получить **PSNodeFile** , используйте командлет Get-AzureBatchNodeFile.</span><span class="sxs-lookup"><span data-stu-id="e992c-133">To obtain a **PSNodeFile** , use the Get-AzureBatchNodeFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSNodeFile
Parameter Sets: InputObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e992c-134">-JobId</span><span class="sxs-lookup"><span data-stu-id="e992c-134">-JobId</span></span>
<span data-ttu-id="e992c-135">Указывает идентификатор задания, содержащего задачу.</span><span class="sxs-lookup"><span data-stu-id="e992c-135">Specifies the ID of the job that contains the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e992c-136">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e992c-136">-Name</span></span>
<span data-ttu-id="e992c-137">Указывает имя файла узла, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="e992c-137">Specifies the name of the node file that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: Task, ComputeNode
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e992c-138">-PoolId</span><span class="sxs-lookup"><span data-stu-id="e992c-138">-PoolId</span></span>
<span data-ttu-id="e992c-139">Указывает ИД пула, содержащего вычислительные узлы, для которых этот командлет удаляет файл.</span><span class="sxs-lookup"><span data-stu-id="e992c-139">Specifies the ID of the pool that contains the compute nodes for which this cmdlet removes a file.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e992c-140">-Recursive</span><span class="sxs-lookup"><span data-stu-id="e992c-140">-Recursive</span></span>
<span data-ttu-id="e992c-141">Указывает на то, что этот командлет удаляет папку и все вложенные папки и файлы по указанному пути.</span><span class="sxs-lookup"><span data-stu-id="e992c-141">Indicates that this cmdlet deletes the folder and all subfolders and files under the specified path.</span></span>
<span data-ttu-id="e992c-142">Этот командлет имеет смысл только в том случае, если путь является папкой.</span><span class="sxs-lookup"><span data-stu-id="e992c-142">This cmdlet is relevant only if the path is a folder.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e992c-143">-TaskId</span><span class="sxs-lookup"><span data-stu-id="e992c-143">-TaskId</span></span>
<span data-ttu-id="e992c-144">Указывает идентификатор задачи.</span><span class="sxs-lookup"><span data-stu-id="e992c-144">Specifies the ID of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e992c-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e992c-145">-Confirm</span></span>
<span data-ttu-id="e992c-146">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e992c-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e992c-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e992c-147">-WhatIf</span></span>
<span data-ttu-id="e992c-148">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e992c-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e992c-149">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e992c-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e992c-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e992c-150">-DefaultProfile</span></span>
<span data-ttu-id="e992c-151">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e992c-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e992c-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e992c-152">CommonParameters</span></span>
<span data-ttu-id="e992c-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e992c-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e992c-154">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e992c-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e992c-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e992c-155">INPUTS</span></span>

### <span data-ttu-id="e992c-156">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e992c-156">BatchAccountContext</span></span>
<span data-ttu-id="e992c-157">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="e992c-157">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="e992c-158">PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="e992c-158">PSNodeFile</span></span>
<span data-ttu-id="e992c-159">Параметр "InputObject" принимает значение типа "PSNodeFile" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="e992c-159">Parameter 'InputObject' accepts value of type 'PSNodeFile' from the pipeline</span></span>

## <span data-ttu-id="e992c-160">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e992c-160">OUTPUTS</span></span>

## <span data-ttu-id="e992c-161">Пуск</span><span class="sxs-lookup"><span data-stu-id="e992c-161">NOTES</span></span>

## <span data-ttu-id="e992c-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e992c-162">RELATED LINKS</span></span>

[<span data-ttu-id="e992c-163">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="e992c-163">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="e992c-164">Get-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="e992c-164">Get-AzureBatchNodeFile</span></span>](./Get-AzureBatchNodeFile.md)

[<span data-ttu-id="e992c-165">Get-AzureBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="e992c-165">Get-AzureBatchNodeFileContent</span></span>](./Get-AzureBatchNodeFileContent.md)


