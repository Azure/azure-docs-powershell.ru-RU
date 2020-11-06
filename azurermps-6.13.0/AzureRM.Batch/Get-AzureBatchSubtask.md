---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 7D0D8B46-4BF0-47D5-9261-3306AEB9E7DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchsubtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchSubtask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchSubtask.md
ms.openlocfilehash: 5aa0ccc7da257cf20deb4a79d2b5415aa4c45885
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567821"
---
# <span data-ttu-id="ae595-101">Get-AzureBatchSubtask</span><span class="sxs-lookup"><span data-stu-id="ae595-101">Get-AzureBatchSubtask</span></span>

## <span data-ttu-id="ae595-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ae595-102">SYNOPSIS</span></span>
<span data-ttu-id="ae595-103">Возвращает сведения о подзадаче для указанной задачи.</span><span class="sxs-lookup"><span data-stu-id="ae595-103">Gets the subtask information of the specified task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae595-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ae595-104">SYNTAX</span></span>

### <span data-ttu-id="ae595-105">ODataFilter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ae595-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchSubtask [-JobId] <String> [-TaskId] <String> [-MaxCount <Int32>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae595-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="ae595-106">ParentObject</span></span>
```
Get-AzureBatchSubtask [[-Task] <PSCloudTask>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae595-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae595-107">DESCRIPTION</span></span>
<span data-ttu-id="ae595-108">Командлет **Get-AzureBatchSubtask** извлекает сведения о подзадаче для указанной задачи.</span><span class="sxs-lookup"><span data-stu-id="ae595-108">The **Get-AzureBatchSubtask** cmdlet retrieves the subtask information about the specified task.</span></span>
<span data-ttu-id="ae595-109">Подзадачи обеспечивают параллельную обработку отдельных задач и обеспечивают точное наблюдение за выполнением и ходом выполнения задач.</span><span class="sxs-lookup"><span data-stu-id="ae595-109">Subtasks provide parallel processing for individual tasks, and enable precise monitoring of task execution and progress.</span></span>

## <span data-ttu-id="ae595-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ae595-110">EXAMPLES</span></span>

### <span data-ttu-id="ae595-111">Пример 1: возврат всех подзадач для указанной задачи</span><span class="sxs-lookup"><span data-stu-id="ae595-111">Example 1: Return all subtasks for a specified task</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzureBatchSubtask -JobId "Job-01" -TaskID "myTask" -BatchContext $Context
```

<span data-ttu-id="ae595-112">Эти команды возвращают все подзадачи для задачи с ИДЕНТИФИКАТОРом myTask.</span><span class="sxs-lookup"><span data-stu-id="ae595-112">These commands return all the subtasks for the task with the ID myTask.</span></span>
<span data-ttu-id="ae595-113">Для этого первой командой в примере создается ссылка на объект для contosobatchaccount учетной записи пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="ae595-113">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="ae595-114">Эта ссылка на объект хранится в переменной с именем $context.</span><span class="sxs-lookup"><span data-stu-id="ae595-114">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="ae595-115">Вторая команда использует ссылку на объект и командлет **Get-AzureBatchSubtask** , чтобы получить все подзадачи для myTask, задачи, которые выполняются как часть задания задания — 01.</span><span class="sxs-lookup"><span data-stu-id="ae595-115">The second command then uses that object reference and the **Get-AzureBatchSubtask** cmdlet to return all the subtasks for myTask, a task that runs as part of job Job-01.</span></span>

## <span data-ttu-id="ae595-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ae595-116">PARAMETERS</span></span>

### <span data-ttu-id="ae595-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ae595-117">-BatchContext</span></span>
<span data-ttu-id="ae595-118">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="ae595-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ae595-119">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="ae595-119">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ae595-120">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="ae595-120">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ae595-121">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="ae595-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ae595-122">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="ae595-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ae595-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae595-123">-DefaultProfile</span></span>
<span data-ttu-id="ae595-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ae595-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae595-125">-JobId</span><span class="sxs-lookup"><span data-stu-id="ae595-125">-JobId</span></span>
<span data-ttu-id="ae595-126">Указывает идентификатор задания, содержащего задачу, подзадачи которой этот командлет получает.</span><span class="sxs-lookup"><span data-stu-id="ae595-126">Specifies the ID of the job that contains the task whose subtasks this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae595-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="ae595-127">-MaxCount</span></span>
<span data-ttu-id="ae595-128">Указывает максимальное число возвращаемых подзадач.</span><span class="sxs-lookup"><span data-stu-id="ae595-128">Specifies the maximum number of subtasks to return.</span></span>
<span data-ttu-id="ae595-129">Если вы задаете нулевое значение (0) или меньше, в командлете не используется верхний предел.</span><span class="sxs-lookup"><span data-stu-id="ae595-129">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="ae595-130">Значение по умолчанию — 1000.</span><span class="sxs-lookup"><span data-stu-id="ae595-130">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae595-131">-Задача</span><span class="sxs-lookup"><span data-stu-id="ae595-131">-Task</span></span>
<span data-ttu-id="ae595-132">Указывает ссылку на объект задачи, которая содержит подзадачи, возвращаемые этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="ae595-132">Specifies an object reference to the task that contain the subtasks that this cmdlet returns.</span></span>
<span data-ttu-id="ae595-133">Эта ссылка на объект создается с помощью командлета Get-AzureBatchTask и сохраняет возвращаемый объект в переменной.</span><span class="sxs-lookup"><span data-stu-id="ae595-133">This object reference is created by using the Get-AzureBatchTask cmdlet and storing the returned object in a variable.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae595-134">-TaskId</span><span class="sxs-lookup"><span data-stu-id="ae595-134">-TaskId</span></span>
<span data-ttu-id="ae595-135">Указывает идентификатор задачи, подзадачи которой возвращает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ae595-135">Specifies the ID of the task whose subtasks this cmdlet returns.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae595-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae595-136">CommonParameters</span></span>
<span data-ttu-id="ae595-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ae595-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae595-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae595-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae595-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ae595-139">INPUTS</span></span>

### <span data-ttu-id="ae595-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ae595-140">System.String</span></span>

### <span data-ttu-id="ae595-141">Microsoft.Azure.Commands.BatCH. Models. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="ae595-141">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>
<span data-ttu-id="ae595-142">Параметры: Task (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ae595-142">Parameters: Task (ByValue)</span></span>

### <span data-ttu-id="ae595-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ae595-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="ae595-144">Параметры: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ae595-144">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="ae595-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae595-145">OUTPUTS</span></span>

### <span data-ttu-id="ae595-146">Microsoft.Azure.Commands.BatCH. Models. PSSubtaskInformation</span><span class="sxs-lookup"><span data-stu-id="ae595-146">Microsoft.Azure.Commands.Batch.Models.PSSubtaskInformation</span></span>

## <span data-ttu-id="ae595-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="ae595-147">NOTES</span></span>

## <span data-ttu-id="ae595-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ae595-148">RELATED LINKS</span></span>

[<span data-ttu-id="ae595-149">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="ae595-149">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)


