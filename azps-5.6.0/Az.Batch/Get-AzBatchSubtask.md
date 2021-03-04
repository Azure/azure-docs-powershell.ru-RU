---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 7D0D8B46-4BF0-47D5-9261-3306AEB9E7DD
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchsubtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSubtask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSubtask.md
ms.openlocfilehash: 622b25a4cd84fcdd6ffb8179b3990ac786733e06
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990478"
---
# <span data-ttu-id="b5e18-101">Get-AzBatchSubtask</span><span class="sxs-lookup"><span data-stu-id="b5e18-101">Get-AzBatchSubtask</span></span>

## <span data-ttu-id="b5e18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5e18-102">SYNOPSIS</span></span>
<span data-ttu-id="b5e18-103">Возвращает сведения о подзадаче для указанной задачи.</span><span class="sxs-lookup"><span data-stu-id="b5e18-103">Gets the subtask information of the specified task.</span></span>

## <span data-ttu-id="b5e18-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b5e18-104">SYNTAX</span></span>

### <span data-ttu-id="b5e18-105">ODataFilter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b5e18-105">ODataFilter (Default)</span></span>
```
Get-AzBatchSubtask [-JobId] <String> [-TaskId] <String> [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5e18-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="b5e18-106">ParentObject</span></span>
```
Get-AzBatchSubtask [[-Task] <PSCloudTask>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5e18-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5e18-107">DESCRIPTION</span></span>
<span data-ttu-id="b5e18-108">Для получения сведений о указанной задаче с его подзадачей извлекается **cmdlet Get-AzBatchSubtask.**</span><span class="sxs-lookup"><span data-stu-id="b5e18-108">The **Get-AzBatchSubtask** cmdlet retrieves the subtask information about the specified task.</span></span>
<span data-ttu-id="b5e18-109">Подзадачи обеспечивают параллельную обработку отдельных задач и позволяют точно следить за выполнением и ходом выполнения задач.</span><span class="sxs-lookup"><span data-stu-id="b5e18-109">Subtasks provide parallel processing for individual tasks, and enable precise monitoring of task execution and progress.</span></span>

## <span data-ttu-id="b5e18-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b5e18-110">EXAMPLES</span></span>

### <span data-ttu-id="b5e18-111">Пример 1. Возврат всех подзадач для указанной задачи</span><span class="sxs-lookup"><span data-stu-id="b5e18-111">Example 1: Return all subtasks for a specified task</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchSubtask -JobId "Job-01" -TaskID "myTask" -BatchContext $Context
```

<span data-ttu-id="b5e18-112">Эти команды возвращают все подзадачи задачи с ID myTask.</span><span class="sxs-lookup"><span data-stu-id="b5e18-112">These commands return all the subtasks for the task with the ID myTask.</span></span>
<span data-ttu-id="b5e18-113">Для этого первая команда из примера создает ссылку на ключи учетных записей для пакетной учетной записи contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="b5e18-113">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="b5e18-114">Эта ссылка на объект хранится в переменной с именем $context.</span><span class="sxs-lookup"><span data-stu-id="b5e18-114">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="b5e18-115">Затем вторая команда использует эту ссылку на объект и командлет **Get-AzBatchSubtask** для возврата всех подзадач myTask — задачи, которая выполняется в рамках задания 01.</span><span class="sxs-lookup"><span data-stu-id="b5e18-115">The second command then uses that object reference and the **Get-AzBatchSubtask** cmdlet to return all the subtasks for myTask, a task that runs as part of job Job-01.</span></span>

## <span data-ttu-id="b5e18-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5e18-116">PARAMETERS</span></span>

### <span data-ttu-id="b5e18-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b5e18-117">-BatchContext</span></span>
<span data-ttu-id="b5e18-118">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="b5e18-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b5e18-119">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой пакета будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b5e18-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b5e18-120">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="b5e18-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b5e18-121">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b5e18-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b5e18-122">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="b5e18-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="b5e18-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5e18-123">-DefaultProfile</span></span>
<span data-ttu-id="b5e18-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b5e18-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5e18-125">-JobId</span><span class="sxs-lookup"><span data-stu-id="b5e18-125">-JobId</span></span>
<span data-ttu-id="b5e18-126">Определяет код задания, содержаща задачу, подзадачи которой получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5e18-126">Specifies the ID of the job that contains the task whose subtasks this cmdlet gets.</span></span>

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

### <span data-ttu-id="b5e18-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="b5e18-127">-MaxCount</span></span>
<span data-ttu-id="b5e18-128">Указывает максимальное количество подзадач, которые нужно вернуть.</span><span class="sxs-lookup"><span data-stu-id="b5e18-128">Specifies the maximum number of subtasks to return.</span></span>
<span data-ttu-id="b5e18-129">Если указать нулевое (ноль) или меньшее значение, для cmdlet не используется верхний предел.</span><span class="sxs-lookup"><span data-stu-id="b5e18-129">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="b5e18-130">Значение по умолчанию — 1000.</span><span class="sxs-lookup"><span data-stu-id="b5e18-130">The default value is 1000.</span></span>

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

### <span data-ttu-id="b5e18-131">-Задача</span><span class="sxs-lookup"><span data-stu-id="b5e18-131">-Task</span></span>
<span data-ttu-id="b5e18-132">Указывает ссылку на объект, который содержит подзадачи, которые возвращает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5e18-132">Specifies an object reference to the task that contain the subtasks that this cmdlet returns.</span></span>
<span data-ttu-id="b5e18-133">Эта ссылка создается с помощью Get-AzBatchTask и хранения возвращаемого объекта в переменной.</span><span class="sxs-lookup"><span data-stu-id="b5e18-133">This object reference is created by using the Get-AzBatchTask cmdlet and storing the returned object in a variable.</span></span>

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

### <span data-ttu-id="b5e18-134">-TaskId</span><span class="sxs-lookup"><span data-stu-id="b5e18-134">-TaskId</span></span>
<span data-ttu-id="b5e18-135">Определяет код задачи, подзадачи которой возвращает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5e18-135">Specifies the ID of the task whose subtasks this cmdlet returns.</span></span>

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

### <span data-ttu-id="b5e18-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5e18-136">CommonParameters</span></span>
<span data-ttu-id="b5e18-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5e18-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5e18-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b5e18-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5e18-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b5e18-139">INPUTS</span></span>

### <span data-ttu-id="b5e18-140">System.String</span><span class="sxs-lookup"><span data-stu-id="b5e18-140">System.String</span></span>

### <span data-ttu-id="b5e18-141">Microsoft.Azure.Commands.Batch. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="b5e18-141">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="b5e18-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b5e18-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="b5e18-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b5e18-143">OUTPUTS</span></span>

### <span data-ttu-id="b5e18-144">Microsoft.Azure.Commands.Batch. Models.PSSubtaskInformation</span><span class="sxs-lookup"><span data-stu-id="b5e18-144">Microsoft.Azure.Commands.Batch.Models.PSSubtaskInformation</span></span>

## <span data-ttu-id="b5e18-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b5e18-145">NOTES</span></span>

## <span data-ttu-id="b5e18-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b5e18-146">RELATED LINKS</span></span>

[<span data-ttu-id="b5e18-147">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="b5e18-147">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)


