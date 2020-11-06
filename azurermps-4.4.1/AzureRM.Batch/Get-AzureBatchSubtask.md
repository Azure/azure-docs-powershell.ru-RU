---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 7D0D8B46-4BF0-47D5-9261-3306AEB9E7DD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchSubtask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchSubtask.md
ms.openlocfilehash: 58bed6fda4040c1af48469f4aa85f717c26c898c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570115"
---
# <span data-ttu-id="fb1da-101">Get-AzureBatchSubtask</span><span class="sxs-lookup"><span data-stu-id="fb1da-101">Get-AzureBatchSubtask</span></span>

## <span data-ttu-id="fb1da-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fb1da-102">SYNOPSIS</span></span>
<span data-ttu-id="fb1da-103">Возвращает сведения о подзадаче для указанной задачи.</span><span class="sxs-lookup"><span data-stu-id="fb1da-103">Gets the subtask information of the specified task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb1da-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fb1da-104">SYNTAX</span></span>

### <span data-ttu-id="fb1da-105">ODataFilter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fb1da-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchSubtask [-JobId] <String> [-TaskId] <String> [-MaxCount <Int32>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb1da-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="fb1da-106">ParentObject</span></span>
```
Get-AzureBatchSubtask [[-Task] <PSCloudTask>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb1da-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb1da-107">DESCRIPTION</span></span>
<span data-ttu-id="fb1da-108">Командлет **Get-AzureBatchSubtask** извлекает сведения о подзадаче для указанной задачи.</span><span class="sxs-lookup"><span data-stu-id="fb1da-108">The **Get-AzureBatchSubtask** cmdlet retrieves the subtask information about the specified task.</span></span>
<span data-ttu-id="fb1da-109">Подзадачи обеспечивают параллельную обработку отдельных задач и обеспечивают точное наблюдение за выполнением и ходом выполнения задач.</span><span class="sxs-lookup"><span data-stu-id="fb1da-109">Subtasks provide parallel processing for individual tasks, and enable precise monitoring of task execution and progress.</span></span>

## <span data-ttu-id="fb1da-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fb1da-110">EXAMPLES</span></span>

### <span data-ttu-id="fb1da-111">Пример 1: возврат всех подзадач для указанной задачи</span><span class="sxs-lookup"><span data-stu-id="fb1da-111">Example 1: Return all subtasks for a specified task</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzureBatchSubtask -JobId "Job-01" -TaskID "myTask" -BatchContext $Context
```

<span data-ttu-id="fb1da-112">Эти команды возвращают все подзадачи для задачи с ИДЕНТИФИКАТОРом myTask.</span><span class="sxs-lookup"><span data-stu-id="fb1da-112">These commands return all the subtasks for the task with the ID myTask.</span></span>
<span data-ttu-id="fb1da-113">Для этого первой командой в примере создается ссылка на объект для contosobatchaccount учетной записи пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="fb1da-113">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="fb1da-114">Эта ссылка на объект хранится в переменной с именем $context.</span><span class="sxs-lookup"><span data-stu-id="fb1da-114">This object reference is stored in a variable named $context.</span></span>

<span data-ttu-id="fb1da-115">Вторая команда использует ссылку на объект и командлет **Get-AzureBatchSubtask** , чтобы получить все подзадачи для myTask, задачи, которые выполняются как часть задания задания — 01.</span><span class="sxs-lookup"><span data-stu-id="fb1da-115">The second command then uses that object reference and the **Get-AzureBatchSubtask** cmdlet to return all the subtasks for myTask, a task that runs as part of job Job-01.</span></span>

## <span data-ttu-id="fb1da-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fb1da-116">PARAMETERS</span></span>

### <span data-ttu-id="fb1da-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="fb1da-117">-BatchContext</span></span>
<span data-ttu-id="fb1da-118">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="fb1da-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="fb1da-119">Чтобы получить объект **BatchAccountContext** , содержащий клавиши доступа для вашей подписки, используйте командлет Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="fb1da-119">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="fb1da-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="fb1da-120">-JobId</span></span>
<span data-ttu-id="fb1da-121">Указывает идентификатор задания, содержащего задачу, подзадачи которой этот командлет получает.</span><span class="sxs-lookup"><span data-stu-id="fb1da-121">Specifies the ID of the job that contains the task whose subtasks this cmdlet gets.</span></span>

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

### <span data-ttu-id="fb1da-122">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="fb1da-122">-MaxCount</span></span>
<span data-ttu-id="fb1da-123">Указывает максимальное число возвращаемых подзадач.</span><span class="sxs-lookup"><span data-stu-id="fb1da-123">Specifies the maximum number of subtasks to return.</span></span>
<span data-ttu-id="fb1da-124">Если вы задаете нулевое значение (0) или меньше, в командлете не используется верхний предел.</span><span class="sxs-lookup"><span data-stu-id="fb1da-124">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="fb1da-125">Значение по умолчанию — 1000.</span><span class="sxs-lookup"><span data-stu-id="fb1da-125">The default value is 1000.</span></span>

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

### <span data-ttu-id="fb1da-126">-Задача</span><span class="sxs-lookup"><span data-stu-id="fb1da-126">-Task</span></span>
<span data-ttu-id="fb1da-127">Указывает ссылку на объект задачи, которая содержит подзадачи, возвращаемые этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="fb1da-127">Specifies an object reference to the task that contain the subtasks that this cmdlet returns.</span></span>
<span data-ttu-id="fb1da-128">Эта ссылка на объект создается с помощью командлета Get-AzureBatchTask и сохраняет возвращаемый объект в переменной.</span><span class="sxs-lookup"><span data-stu-id="fb1da-128">This object reference is created by using the Get-AzureBatchTask cmdlet and storing the returned object in a variable.</span></span>

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

### <span data-ttu-id="fb1da-129">-TaskId</span><span class="sxs-lookup"><span data-stu-id="fb1da-129">-TaskId</span></span>
<span data-ttu-id="fb1da-130">Указывает идентификатор задачи, подзадачи которой возвращает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="fb1da-130">Specifies the ID of the task whose subtasks this cmdlet returns.</span></span>

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

### <span data-ttu-id="fb1da-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb1da-131">-DefaultProfile</span></span>
<span data-ttu-id="fb1da-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fb1da-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb1da-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb1da-133">CommonParameters</span></span>
<span data-ttu-id="fb1da-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fb1da-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb1da-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb1da-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb1da-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fb1da-136">INPUTS</span></span>

### <span data-ttu-id="fb1da-137">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="fb1da-137">BatchAccountContext</span></span>
<span data-ttu-id="fb1da-138">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="fb1da-138">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="fb1da-139">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="fb1da-139">PSCloudTask</span></span>
<span data-ttu-id="fb1da-140">Параметр "задача" принимает значение типа "PSCloudTask" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="fb1da-140">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="fb1da-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb1da-141">OUTPUTS</span></span>

###  
<span data-ttu-id="fb1da-142">Этот командлет возвращает экземпляры объекта **PSSubtaskInformation** .</span><span class="sxs-lookup"><span data-stu-id="fb1da-142">This cmdlet returns instances of the **PSSubtaskInformation** object.</span></span>

## <span data-ttu-id="fb1da-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="fb1da-143">NOTES</span></span>

## <span data-ttu-id="fb1da-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fb1da-144">RELATED LINKS</span></span>

[<span data-ttu-id="fb1da-145">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="fb1da-145">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)


