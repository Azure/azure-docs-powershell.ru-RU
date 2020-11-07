---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: DBA02017-8372-4A91-A4F1-985777DEDAB9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchnodefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchNodeFile.md
ms.openlocfilehash: a81d77ac1761c37dc3042394a4a70bda6848cc83
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732487"
---
# <span data-ttu-id="70925-101">Remove-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="70925-101">Remove-AzureBatchNodeFile</span></span>

## <span data-ttu-id="70925-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="70925-102">SYNOPSIS</span></span>
<span data-ttu-id="70925-103">Удаляет файл узла для задачи или вычислительного узла.</span><span class="sxs-lookup"><span data-stu-id="70925-103">Deletes a node file for a task or compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70925-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="70925-104">SYNTAX</span></span>

### <span data-ttu-id="70925-105">Задачи</span><span class="sxs-lookup"><span data-stu-id="70925-105">Task</span></span>
```
Remove-AzureBatchNodeFile -JobId <String> -TaskId <String> -Path <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="70925-106">ComputeNode</span><span class="sxs-lookup"><span data-stu-id="70925-106">ComputeNode</span></span>
```
Remove-AzureBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> -Path <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="70925-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="70925-107">InputObject</span></span>
```
Remove-AzureBatchNodeFile [[-InputObject] <PSNodeFile>] [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="70925-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="70925-108">DESCRIPTION</span></span>
<span data-ttu-id="70925-109">Командлет **Remove-AzureBatchNodeFile** удаляет пакетный файл узла Azure для задачи или вычислительного узла.</span><span class="sxs-lookup"><span data-stu-id="70925-109">The **Remove-AzureBatchNodeFile** cmdlet deletes an Azure Batch node file for a task or compute node.</span></span>

## <span data-ttu-id="70925-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="70925-110">EXAMPLES</span></span>

### <span data-ttu-id="70925-111">Пример 1: удаление файла, assocated с задачей</span><span class="sxs-lookup"><span data-stu-id="70925-111">Example 1: Delete a file assocated with a task</span></span>
```
PS C:\>Remove-AzureBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "wd\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="70925-112">Эта команда удаляет файл узла с именем wd\testFile.txt.</span><span class="sxs-lookup"><span data-stu-id="70925-112">This command deletes the node file that is named wd\testFile.txt.</span></span>
<span data-ttu-id="70925-113">Этот файл связан с задачей, которая имеет идентификатор Task26 под заданием задания — 000001.</span><span class="sxs-lookup"><span data-stu-id="70925-113">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>

### <span data-ttu-id="70925-114">Пример 2: удаление файла из вычислительного узла</span><span class="sxs-lookup"><span data-stu-id="70925-114">Example 2: Delete a file from a compute node</span></span>
```
PS C:\>Remove-AzureBatchNodeFile -PoolId "Pool07" -ComputeNodeId "tvm-2316545714_1-20150725t213220z" -Path "startup\testFile.txt" -BatchContext $Context
```

<span data-ttu-id="70925-115">Эта команда удаляет файл узла с именем startup\testFile.txt из указанного вычислительного узла в пуле с ИДЕНТИФИКАТОРом Pool07.</span><span class="sxs-lookup"><span data-stu-id="70925-115">This command deletes the node file that is named startup\testFile.txt from the specified compute node in the pool that has the ID Pool07.</span></span>

### <span data-ttu-id="70925-116">Пример 3: удаление файла с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="70925-116">Example 3: Remove a file by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "wd\testFile2.txt" -BatchContext $Context | Remove-AzureBatchNodeFile -Force -BatchContext $Context
```

<span data-ttu-id="70925-117">Эта команда получает файл узла с помощью **Get-AzureBatchNodeFile**.</span><span class="sxs-lookup"><span data-stu-id="70925-117">This command gets the node file by using **Get-AzureBatchNodeFile**.</span></span>
<span data-ttu-id="70925-118">Этот файл связан с задачей, которая имеет идентификатор Task26 под заданием задания — 000001.</span><span class="sxs-lookup"><span data-stu-id="70925-118">That file is associated with the task that has the ID Task26 under the job Job-000001.</span></span>
<span data-ttu-id="70925-119">Команда передает этот файл текущему командлету с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="70925-119">The command passes that file to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="70925-120">Текущий командлет удаляет файл узла.</span><span class="sxs-lookup"><span data-stu-id="70925-120">The current cmdlet removes the node file.</span></span>
<span data-ttu-id="70925-121">Команда задает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="70925-121">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="70925-122">Таким образом, команда не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="70925-122">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="70925-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="70925-123">PARAMETERS</span></span>

### <span data-ttu-id="70925-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="70925-124">-BatchContext</span></span>
<span data-ttu-id="70925-125">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="70925-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="70925-126">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="70925-126">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="70925-127">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="70925-127">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="70925-128">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="70925-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="70925-129">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="70925-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="70925-130">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="70925-130">-ComputeNodeId</span></span>
<span data-ttu-id="70925-131">Указывает идентификатор вычислительного узла, содержащего файл узла пакета, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="70925-131">Specifies the ID of the compute node that contains the Batch node file that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="70925-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70925-132">-DefaultProfile</span></span>
<span data-ttu-id="70925-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="70925-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70925-134">-Force</span><span class="sxs-lookup"><span data-stu-id="70925-134">-Force</span></span>
<span data-ttu-id="70925-135">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="70925-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="70925-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70925-136">-InputObject</span></span>
<span data-ttu-id="70925-137">Указывает объект **PSNodeFile** , представляющий файл узла, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="70925-137">Specifies **PSNodeFile** object that represent the node file that this cmdlet deletes.</span></span>
<span data-ttu-id="70925-138">Чтобы получить **PSNodeFile** , используйте командлет Get-AzureBatchNodeFile.</span><span class="sxs-lookup"><span data-stu-id="70925-138">To obtain a **PSNodeFile** , use the Get-AzureBatchNodeFile cmdlet.</span></span>

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

### <span data-ttu-id="70925-139">-JobId</span><span class="sxs-lookup"><span data-stu-id="70925-139">-JobId</span></span>
<span data-ttu-id="70925-140">Указывает идентификатор задания, содержащего задачу.</span><span class="sxs-lookup"><span data-stu-id="70925-140">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="70925-141">-Path</span><span class="sxs-lookup"><span data-stu-id="70925-141">-Path</span></span>
<span data-ttu-id="70925-142">Путь к файлу для удаляемого файла узла.</span><span class="sxs-lookup"><span data-stu-id="70925-142">The file path of the node file to delete.</span></span>

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

### <span data-ttu-id="70925-143">-PoolId</span><span class="sxs-lookup"><span data-stu-id="70925-143">-PoolId</span></span>
<span data-ttu-id="70925-144">Указывает ИД пула, содержащего вычислительные узлы, для которых этот командлет удаляет файл.</span><span class="sxs-lookup"><span data-stu-id="70925-144">Specifies the ID of the pool that contains the compute nodes for which this cmdlet removes a file.</span></span>

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

### <span data-ttu-id="70925-145">-Recursive</span><span class="sxs-lookup"><span data-stu-id="70925-145">-Recursive</span></span>
<span data-ttu-id="70925-146">Указывает на то, что этот командлет удаляет папку и все вложенные папки и файлы по указанному пути.</span><span class="sxs-lookup"><span data-stu-id="70925-146">Indicates that this cmdlet deletes the folder and all subfolders and files under the specified path.</span></span>
<span data-ttu-id="70925-147">Этот командлет имеет смысл только в том случае, если путь является папкой.</span><span class="sxs-lookup"><span data-stu-id="70925-147">This cmdlet is relevant only if the path is a folder.</span></span>

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

### <span data-ttu-id="70925-148">-TaskId</span><span class="sxs-lookup"><span data-stu-id="70925-148">-TaskId</span></span>
<span data-ttu-id="70925-149">Указывает идентификатор задачи.</span><span class="sxs-lookup"><span data-stu-id="70925-149">Specifies the ID of the task.</span></span>

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

### <span data-ttu-id="70925-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="70925-150">-Confirm</span></span>
<span data-ttu-id="70925-151">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="70925-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70925-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70925-152">-WhatIf</span></span>
<span data-ttu-id="70925-153">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="70925-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70925-154">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="70925-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70925-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70925-155">CommonParameters</span></span>
<span data-ttu-id="70925-156">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="70925-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70925-157">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70925-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70925-158">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="70925-158">INPUTS</span></span>

### <span data-ttu-id="70925-159">System. String</span><span class="sxs-lookup"><span data-stu-id="70925-159">System.String</span></span>

### <span data-ttu-id="70925-160">Microsoft.Azure.Commands.BatCH. Models. PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="70925-160">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>
<span data-ttu-id="70925-161">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="70925-161">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="70925-162">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="70925-162">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="70925-163">Параметры: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="70925-163">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="70925-164">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="70925-164">OUTPUTS</span></span>

### <span data-ttu-id="70925-165">System. void</span><span class="sxs-lookup"><span data-stu-id="70925-165">System.Void</span></span>

## <span data-ttu-id="70925-166">Пуск</span><span class="sxs-lookup"><span data-stu-id="70925-166">NOTES</span></span>

## <span data-ttu-id="70925-167">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="70925-167">RELATED LINKS</span></span>

[<span data-ttu-id="70925-168">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="70925-168">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="70925-169">Get-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="70925-169">Get-AzureBatchNodeFile</span></span>](./Get-AzureBatchNodeFile.md)

[<span data-ttu-id="70925-170">Get-AzureBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="70925-170">Get-AzureBatchNodeFileContent</span></span>](./Get-AzureBatchNodeFileContent.md)


