---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DBA02017-8372-4A91-A4F1-985777DEDAB9
online version: https://docs.microsoft.com/powershell/module/az.batch/remove-azbatchnodefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchNodeFile.md
ms.openlocfilehash: a56b8d0613946b33629fda46cc710cdbeef0814e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010888"
---
# <span data-ttu-id="84e0e-101">Remove-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="84e0e-101">Remove-AzBatchNodeFile</span></span>

## <span data-ttu-id="84e0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84e0e-102">SYNOPSIS</span></span>
<span data-ttu-id="84e0e-103">Удаляет файл узла для узла задачи или узла вычислений.</span><span class="sxs-lookup"><span data-stu-id="84e0e-103">Deletes a node file for a task or compute node.</span></span>

## <span data-ttu-id="84e0e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="84e0e-104">SYNTAX</span></span>

### <span data-ttu-id="84e0e-105">Задача</span><span class="sxs-lookup"><span data-stu-id="84e0e-105">Task</span></span>
```
Remove-AzBatchNodeFile -JobId <String> -TaskId <String> -Path <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="84e0e-106">ComputeNode</span><span class="sxs-lookup"><span data-stu-id="84e0e-106">ComputeNode</span></span>
```
Remove-AzBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> -Path <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="84e0e-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="84e0e-107">InputObject</span></span>
```
Remove-AzBatchNodeFile [[-InputObject] <PSNodeFile>] [-Force] [-Recursive] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84e0e-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="84e0e-108">DESCRIPTION</span></span>
<span data-ttu-id="84e0e-109">С **его использованием** удаляется пакетный файл узла Azure для задачи или узла вычислений.</span><span class="sxs-lookup"><span data-stu-id="84e0e-109">The **Remove-AzBatchNodeFile** cmdlet deletes an Azure Batch node file for a task or compute node.</span></span>

## <span data-ttu-id="84e0e-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="84e0e-110">EXAMPLES</span></span>

### <span data-ttu-id="84e0e-111">Пример 1. Удаление файла, связанного с задачей</span><span class="sxs-lookup"><span data-stu-id="84e0e-111">Example 1: Delete a file associated with a task</span></span>
```
PS C:\>Remove-AzBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "wd\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="84e0e-112">Эта команда удаляет файл узла с именем wd\testFile.txt.</span><span class="sxs-lookup"><span data-stu-id="84e0e-112">This command deletes the node file that is named wd\testFile.txt.</span></span>
<span data-ttu-id="84e0e-113">Этот файл связан с задачей, которая имеет задачу "ID Task26" в рамках задания-0000001.</span><span class="sxs-lookup"><span data-stu-id="84e0e-113">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>

### <span data-ttu-id="84e0e-114">Пример 2. Удаление файла из узла вычислений</span><span class="sxs-lookup"><span data-stu-id="84e0e-114">Example 2: Delete a file from a compute node</span></span>
```
PS C:\>Remove-AzBatchNodeFile -PoolId "Pool07" -ComputeNodeId "tvm-2316545714_1-20150725t213220z" -Path "startup\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="84e0e-115">Эта команда удаляет файл узла с именем startup\testFile.txt из указанного узла вычислений в пуле, который содержит пул ID Pool07.</span><span class="sxs-lookup"><span data-stu-id="84e0e-115">This command deletes the node file that is named startup\testFile.txt from the specified compute node in the pool that has the ID Pool07.</span></span>

### <span data-ttu-id="84e0e-116">Пример 3. Удаление файла с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="84e0e-116">Example 3: Remove a file by using the pipeline</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "wd\testFile2.txt" -BatchContext $Context | Remove-AzBatchNodeFile -Force -BatchContext $Context
```

<span data-ttu-id="84e0e-117">Эта команда получает файл узла с помощью **Get-AzBatchNodeFile.**</span><span class="sxs-lookup"><span data-stu-id="84e0e-117">This command gets the node file by using **Get-AzBatchNodeFile**.</span></span>
<span data-ttu-id="84e0e-118">Этот файл связан с задачей, которая имеет задачу "ID Task26" в рамках задания-0000001.</span><span class="sxs-lookup"><span data-stu-id="84e0e-118">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>
<span data-ttu-id="84e0e-119">Эта команда передает этот файл текущему командлету с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="84e0e-119">The command passes that file to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="84e0e-120">Текущий cmdlet удаляет файл узла.</span><span class="sxs-lookup"><span data-stu-id="84e0e-120">The current cmdlet removes the node file.</span></span>
<span data-ttu-id="84e0e-121">Команда определяет параметр *Force.*</span><span class="sxs-lookup"><span data-stu-id="84e0e-121">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="84e0e-122">Таким образом, команда не будет запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="84e0e-122">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="84e0e-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="84e0e-123">PARAMETERS</span></span>

### <span data-ttu-id="84e0e-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="84e0e-124">-BatchContext</span></span>
<span data-ttu-id="84e0e-125">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="84e0e-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="84e0e-126">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой batchy будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="84e0e-126">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="84e0e-127">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="84e0e-127">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="84e0e-128">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="84e0e-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="84e0e-129">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="84e0e-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="84e0e-130">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="84e0e-130">-ComputeNodeId</span></span>
<span data-ttu-id="84e0e-131">Определяет код узла вычислений, содержаного пакетный файл узла, который удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84e0e-131">Specifies the ID of the compute node that contains the Batch node file that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="84e0e-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84e0e-132">-DefaultProfile</span></span>
<span data-ttu-id="84e0e-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="84e0e-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84e0e-134">-Force</span><span class="sxs-lookup"><span data-stu-id="84e0e-134">-Force</span></span>
<span data-ttu-id="84e0e-135">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="84e0e-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="84e0e-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84e0e-136">-InputObject</span></span>
<span data-ttu-id="84e0e-137">Определяет объект **PSNodeFile,** представляюща файл узла, который удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84e0e-137">Specifies **PSNodeFile** object that represent the node file that this cmdlet deletes.</span></span>
<span data-ttu-id="84e0e-138">Чтобы получить **PSNodeFile,** используйте Get-AzBatchNodeFile..</span><span class="sxs-lookup"><span data-stu-id="84e0e-138">To obtain a **PSNodeFile**, use the Get-AzBatchNodeFile cmdlet.</span></span>

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

### <span data-ttu-id="84e0e-139">-JobId</span><span class="sxs-lookup"><span data-stu-id="84e0e-139">-JobId</span></span>
<span data-ttu-id="84e0e-140">Определяет ИД задания, которое содержит задачу.</span><span class="sxs-lookup"><span data-stu-id="84e0e-140">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="84e0e-141">-Path</span><span class="sxs-lookup"><span data-stu-id="84e0e-141">-Path</span></span>
<span data-ttu-id="84e0e-142">Путь к файлу узла, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="84e0e-142">The file path of the node file to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: Task, ComputeNode
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84e0e-143">-PoolId</span><span class="sxs-lookup"><span data-stu-id="84e0e-143">-PoolId</span></span>
<span data-ttu-id="84e0e-144">Определяет код пула, который содержит узлы компьютеров, для которых этот cmdlet удаляет файл.</span><span class="sxs-lookup"><span data-stu-id="84e0e-144">Specifies the ID of the pool that contains the compute nodes for which this cmdlet removes a file.</span></span>

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

### <span data-ttu-id="84e0e-145">-Recursive</span><span class="sxs-lookup"><span data-stu-id="84e0e-145">-Recursive</span></span>
<span data-ttu-id="84e0e-146">Указывает на то, что этот cmdlet удаляет папку, а также все вложенные папки и файлы, указанные по указанному пути.</span><span class="sxs-lookup"><span data-stu-id="84e0e-146">Indicates that this cmdlet deletes the folder and all subfolders and files under the specified path.</span></span>
<span data-ttu-id="84e0e-147">Этот cmdlet is relevant only if the path is a folder.</span><span class="sxs-lookup"><span data-stu-id="84e0e-147">This cmdlet is relevant only if the path is a folder.</span></span>

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

### <span data-ttu-id="84e0e-148">-TaskId</span><span class="sxs-lookup"><span data-stu-id="84e0e-148">-TaskId</span></span>
<span data-ttu-id="84e0e-149">Определяет ИД задачи.</span><span class="sxs-lookup"><span data-stu-id="84e0e-149">Specifies the ID of the task.</span></span>

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

### <span data-ttu-id="84e0e-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="84e0e-150">-Confirm</span></span>
<span data-ttu-id="84e0e-151">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84e0e-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84e0e-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84e0e-152">-WhatIf</span></span>
<span data-ttu-id="84e0e-153">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84e0e-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84e0e-154">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="84e0e-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84e0e-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84e0e-155">CommonParameters</span></span>
<span data-ttu-id="84e0e-156">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84e0e-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84e0e-157">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="84e0e-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84e0e-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="84e0e-158">INPUTS</span></span>

### <span data-ttu-id="84e0e-159">System.String</span><span class="sxs-lookup"><span data-stu-id="84e0e-159">System.String</span></span>

### <span data-ttu-id="84e0e-160">Microsoft.Azure.Commands.Batch. Models.PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="84e0e-160">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>

### <span data-ttu-id="84e0e-161">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="84e0e-161">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="84e0e-162">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="84e0e-162">OUTPUTS</span></span>

### <span data-ttu-id="84e0e-163">System.Void</span><span class="sxs-lookup"><span data-stu-id="84e0e-163">System.Void</span></span>

## <span data-ttu-id="84e0e-164">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="84e0e-164">NOTES</span></span>

## <span data-ttu-id="84e0e-165">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="84e0e-165">RELATED LINKS</span></span>

[<span data-ttu-id="84e0e-166">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="84e0e-166">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="84e0e-167">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="84e0e-167">Get-AzBatchNodeFile</span></span>](./Get-AzBatchNodeFile.md)

[<span data-ttu-id="84e0e-168">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="84e0e-168">Get-AzBatchNodeFileContent</span></span>](./Get-AzBatchNodeFileContent.md)


