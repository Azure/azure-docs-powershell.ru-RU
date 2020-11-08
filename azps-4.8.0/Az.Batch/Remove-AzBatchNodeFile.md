---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DBA02017-8372-4A91-A4F1-985777DEDAB9
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchnodefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchNodeFile.md
ms.openlocfilehash: 7e9aeebebfc5720ab006d43071eadeabe6bcf655
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079184"
---
# <span data-ttu-id="63491-101">Remove-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="63491-101">Remove-AzBatchNodeFile</span></span>

## <span data-ttu-id="63491-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="63491-102">SYNOPSIS</span></span>
<span data-ttu-id="63491-103">Удаляет файл узла для задачи или вычислительного узла.</span><span class="sxs-lookup"><span data-stu-id="63491-103">Deletes a node file for a task or compute node.</span></span>

## <span data-ttu-id="63491-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="63491-104">SYNTAX</span></span>

### <span data-ttu-id="63491-105">Задачи</span><span class="sxs-lookup"><span data-stu-id="63491-105">Task</span></span>
```
Remove-AzBatchNodeFile -JobId <String> -TaskId <String> -Path <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="63491-106">ComputeNode</span><span class="sxs-lookup"><span data-stu-id="63491-106">ComputeNode</span></span>
```
Remove-AzBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> -Path <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="63491-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="63491-107">InputObject</span></span>
```
Remove-AzBatchNodeFile [[-InputObject] <PSNodeFile>] [-Force] [-Recursive] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63491-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="63491-108">DESCRIPTION</span></span>
<span data-ttu-id="63491-109">Командлет **Remove-AzBatchNodeFile** удаляет пакетный файл узла Azure для задачи или вычислительного узла.</span><span class="sxs-lookup"><span data-stu-id="63491-109">The **Remove-AzBatchNodeFile** cmdlet deletes an Azure Batch node file for a task or compute node.</span></span>

## <span data-ttu-id="63491-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="63491-110">EXAMPLES</span></span>

### <span data-ttu-id="63491-111">Пример 1: удаление файла, связанного с задачей</span><span class="sxs-lookup"><span data-stu-id="63491-111">Example 1: Delete a file associated with a task</span></span>
```
PS C:\>Remove-AzBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "wd\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="63491-112">Эта команда удаляет файл узла с именем wd\testFile.txt.</span><span class="sxs-lookup"><span data-stu-id="63491-112">This command deletes the node file that is named wd\testFile.txt.</span></span>
<span data-ttu-id="63491-113">Этот файл связан с задачей, которая имеет идентификатор Task26 под заданием задания — 000001.</span><span class="sxs-lookup"><span data-stu-id="63491-113">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>

### <span data-ttu-id="63491-114">Пример 2: удаление файла из вычислительного узла</span><span class="sxs-lookup"><span data-stu-id="63491-114">Example 2: Delete a file from a compute node</span></span>
```
PS C:\>Remove-AzBatchNodeFile -PoolId "Pool07" -ComputeNodeId "tvm-2316545714_1-20150725t213220z" -Path "startup\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="63491-115">Эта команда удаляет файл узла с именем startup\testFile.txt из указанного вычислительного узла в пуле с ИДЕНТИФИКАТОРом Pool07.</span><span class="sxs-lookup"><span data-stu-id="63491-115">This command deletes the node file that is named startup\testFile.txt from the specified compute node in the pool that has the ID Pool07.</span></span>

### <span data-ttu-id="63491-116">Пример 3: удаление файла с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="63491-116">Example 3: Remove a file by using the pipeline</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "wd\testFile2.txt" -BatchContext $Context | Remove-AzBatchNodeFile -Force -BatchContext $Context
```

<span data-ttu-id="63491-117">Эта команда получает файл узла с помощью **Get-AzBatchNodeFile**.</span><span class="sxs-lookup"><span data-stu-id="63491-117">This command gets the node file by using **Get-AzBatchNodeFile**.</span></span>
<span data-ttu-id="63491-118">Этот файл связан с задачей, которая имеет идентификатор Task26 под заданием задания — 000001.</span><span class="sxs-lookup"><span data-stu-id="63491-118">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>
<span data-ttu-id="63491-119">Команда передает этот файл текущему командлету с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="63491-119">The command passes that file to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="63491-120">Текущий командлет удаляет файл узла.</span><span class="sxs-lookup"><span data-stu-id="63491-120">The current cmdlet removes the node file.</span></span>
<span data-ttu-id="63491-121">Команда задает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="63491-121">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="63491-122">Таким образом, команда не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="63491-122">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="63491-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="63491-123">PARAMETERS</span></span>

### <span data-ttu-id="63491-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="63491-124">-BatchContext</span></span>
<span data-ttu-id="63491-125">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="63491-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="63491-126">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="63491-126">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="63491-127">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKey, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="63491-127">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="63491-128">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="63491-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="63491-129">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="63491-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="63491-130">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="63491-130">-ComputeNodeId</span></span>
<span data-ttu-id="63491-131">Указывает идентификатор вычислительного узла, содержащего файл узла пакета, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="63491-131">Specifies the ID of the compute node that contains the Batch node file that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="63491-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63491-132">-DefaultProfile</span></span>
<span data-ttu-id="63491-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="63491-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63491-134">-Force</span><span class="sxs-lookup"><span data-stu-id="63491-134">-Force</span></span>
<span data-ttu-id="63491-135">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="63491-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="63491-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63491-136">-InputObject</span></span>
<span data-ttu-id="63491-137">Указывает объект **PSNodeFile** , представляющий файл узла, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="63491-137">Specifies **PSNodeFile** object that represent the node file that this cmdlet deletes.</span></span>
<span data-ttu-id="63491-138">Чтобы получить **PSNodeFile** , используйте командлет Get-AzBatchNodeFile.</span><span class="sxs-lookup"><span data-stu-id="63491-138">To obtain a **PSNodeFile** , use the Get-AzBatchNodeFile cmdlet.</span></span>

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

### <span data-ttu-id="63491-139">-JobId</span><span class="sxs-lookup"><span data-stu-id="63491-139">-JobId</span></span>
<span data-ttu-id="63491-140">Указывает идентификатор задания, содержащего задачу.</span><span class="sxs-lookup"><span data-stu-id="63491-140">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="63491-141">-Path</span><span class="sxs-lookup"><span data-stu-id="63491-141">-Path</span></span>
<span data-ttu-id="63491-142">Путь к файлу для удаляемого файла узла.</span><span class="sxs-lookup"><span data-stu-id="63491-142">The file path of the node file to delete.</span></span>

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

### <span data-ttu-id="63491-143">-PoolId</span><span class="sxs-lookup"><span data-stu-id="63491-143">-PoolId</span></span>
<span data-ttu-id="63491-144">Указывает ИД пула, содержащего вычислительные узлы, для которых этот командлет удаляет файл.</span><span class="sxs-lookup"><span data-stu-id="63491-144">Specifies the ID of the pool that contains the compute nodes for which this cmdlet removes a file.</span></span>

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

### <span data-ttu-id="63491-145">-Recursive</span><span class="sxs-lookup"><span data-stu-id="63491-145">-Recursive</span></span>
<span data-ttu-id="63491-146">Указывает на то, что этот командлет удаляет папку и все вложенные папки и файлы по указанному пути.</span><span class="sxs-lookup"><span data-stu-id="63491-146">Indicates that this cmdlet deletes the folder and all subfolders and files under the specified path.</span></span>
<span data-ttu-id="63491-147">Этот командлет имеет смысл только в том случае, если путь является папкой.</span><span class="sxs-lookup"><span data-stu-id="63491-147">This cmdlet is relevant only if the path is a folder.</span></span>

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

### <span data-ttu-id="63491-148">-TaskId</span><span class="sxs-lookup"><span data-stu-id="63491-148">-TaskId</span></span>
<span data-ttu-id="63491-149">Указывает идентификатор задачи.</span><span class="sxs-lookup"><span data-stu-id="63491-149">Specifies the ID of the task.</span></span>

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

### <span data-ttu-id="63491-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="63491-150">-Confirm</span></span>
<span data-ttu-id="63491-151">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="63491-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63491-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63491-152">-WhatIf</span></span>
<span data-ttu-id="63491-153">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="63491-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63491-154">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="63491-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63491-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63491-155">CommonParameters</span></span>
<span data-ttu-id="63491-156">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="63491-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63491-157">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63491-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63491-158">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="63491-158">INPUTS</span></span>

### <span data-ttu-id="63491-159">System. String</span><span class="sxs-lookup"><span data-stu-id="63491-159">System.String</span></span>

### <span data-ttu-id="63491-160">Microsoft.Azure.Commands.BatCH. Models. PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="63491-160">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>

### <span data-ttu-id="63491-161">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="63491-161">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="63491-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="63491-162">OUTPUTS</span></span>

### <span data-ttu-id="63491-163">System. void</span><span class="sxs-lookup"><span data-stu-id="63491-163">System.Void</span></span>

## <span data-ttu-id="63491-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="63491-164">NOTES</span></span>

## <span data-ttu-id="63491-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="63491-165">RELATED LINKS</span></span>

[<span data-ttu-id="63491-166">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="63491-166">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="63491-167">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="63491-167">Get-AzBatchNodeFile</span></span>](./Get-AzBatchNodeFile.md)

[<span data-ttu-id="63491-168">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="63491-168">Get-AzBatchNodeFileContent</span></span>](./Get-AzBatchNodeFileContent.md)

