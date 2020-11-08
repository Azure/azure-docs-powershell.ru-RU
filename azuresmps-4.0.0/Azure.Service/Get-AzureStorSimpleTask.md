---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: CF3548F6-03FE-44D6-AA2C-1015611C657A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0423fe51a047385ef6395075dd116b4d4189c667
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075552"
---
# <span data-ttu-id="20faa-101">Get-AzureStorSimpleTask</span><span class="sxs-lookup"><span data-stu-id="20faa-101">Get-AzureStorSimpleTask</span></span>

## <span data-ttu-id="20faa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="20faa-102">SYNOPSIS</span></span>
<span data-ttu-id="20faa-103">Возвращает состояние задачи на устройстве StorSimple.</span><span class="sxs-lookup"><span data-stu-id="20faa-103">Gets status of a task on a StorSimple device.</span></span>

## <span data-ttu-id="20faa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="20faa-104">SYNTAX</span></span>

```
Get-AzureStorSimpleTask -InstanceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="20faa-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="20faa-105">DESCRIPTION</span></span>
<span data-ttu-id="20faa-106">Командлет **Get-AzureStorSimpleTask** получает состояние задачи, которая выполняется асинхронно на устройстве Azure StorSimple.</span><span class="sxs-lookup"><span data-stu-id="20faa-106">The **Get-AzureStorSimpleTask** cmdlet retrieves the status of a task that runs asynchronously on an Azure StorSimple device.</span></span>

<span data-ttu-id="20faa-107">При управлении устройством StorSimple большинство операций создания, чтения, обновления и удаления могут выполняться асинхронно.</span><span class="sxs-lookup"><span data-stu-id="20faa-107">While you manage a StorSimple device, most create, read, update, and delete actions can run asynchronously.</span></span>
<span data-ttu-id="20faa-108">Windows PowerShell возвращает элемент **taskId**.</span><span class="sxs-lookup"><span data-stu-id="20faa-108">Windows PowerShell returns a **TaskId**.</span></span>
<span data-ttu-id="20faa-109">Используйте идентификатор, чтобы получить текущее состояние задачи.</span><span class="sxs-lookup"><span data-stu-id="20faa-109">Use the ID to get the current status of the task.</span></span>

## <span data-ttu-id="20faa-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="20faa-110">EXAMPLES</span></span>

### <span data-ttu-id="20faa-111">Пример 1: получение состояния задачи</span><span class="sxs-lookup"><span data-stu-id="20faa-111">Example 1: Get the status of a task</span></span>
```
PS C:\>Get-AzureStorSimpleTask -TaskId "53816d8d-a8b5-4c1d-a177-e59007608d6d"
VERBOSE: ClientRequestId: d9c1e8a7-994f-4698-8b42-064600b45cad_PS
VERBOSE: ClientRequestId: aae17c82-6fd3-435e-a965-1c66b3c955fe_PS


AsyncTaskAggregatedResult : Succeeded
Error                     : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
Result                    : Succeeded
Status                    : Completed
TaskId                    : 53816d8d-a8b5-4c1d-a177-e59007608d6d
TaskSteps                 : {}
StatusCode                : OK
RequestId                 : e9174990825750bba69383748f23019c
```

<span data-ttu-id="20faa-112">Эта команда возвращает состояние задачи с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="20faa-112">This command gets the status of the task that has the specified ID.</span></span>
<span data-ttu-id="20faa-113">Результат показывает, что задача имеет состояние завершено и является результатом успеха.</span><span class="sxs-lookup"><span data-stu-id="20faa-113">The results show that the task has a status of completed and a result of successful.</span></span>

## <span data-ttu-id="20faa-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="20faa-114">PARAMETERS</span></span>

### <span data-ttu-id="20faa-115">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="20faa-115">-InstanceId</span></span>
<span data-ttu-id="20faa-116">Указывает идентификатор задачи, для которой этот командлет отслеживает состояние.</span><span class="sxs-lookup"><span data-stu-id="20faa-116">Specifies the ID of the task for which this cmdlet tracks status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TaskId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20faa-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="20faa-117">-Profile</span></span>
<span data-ttu-id="20faa-118">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="20faa-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="20faa-119">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="20faa-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20faa-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20faa-120">CommonParameters</span></span>
<span data-ttu-id="20faa-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="20faa-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20faa-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20faa-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20faa-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="20faa-123">INPUTS</span></span>

### <span data-ttu-id="20faa-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="20faa-124">None</span></span>

## <span data-ttu-id="20faa-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="20faa-125">OUTPUTS</span></span>

### <span data-ttu-id="20faa-126">JobStatusInfo</span><span class="sxs-lookup"><span data-stu-id="20faa-126">JobStatusInfo</span></span>
<span data-ttu-id="20faa-127">Этот командлет возвращает объект **TaskStatusInfo** , который включает следующие поля:</span><span class="sxs-lookup"><span data-stu-id="20faa-127">This cmdlet returns a **TaskStatusInfo** object which contains the following fields:</span></span> 

- <span data-ttu-id="20faa-128">**Ошибка**.</span><span class="sxs-lookup"><span data-stu-id="20faa-128">**Error**.</span></span>
<span data-ttu-id="20faa-129">**ErrorDetails** , который включает **код** и **сообщение**.</span><span class="sxs-lookup"><span data-stu-id="20faa-129">**ErrorDetails** , which contains **Code** and **Message**.</span></span>
- <span data-ttu-id="20faa-130">**TaskId**.</span><span class="sxs-lookup"><span data-stu-id="20faa-130">**TaskId**.</span></span>
<span data-ttu-id="20faa-131">**String**.</span><span class="sxs-lookup"><span data-stu-id="20faa-131">**String**.</span></span>
<span data-ttu-id="20faa-132">Идентификатор задачи, для которой возвращается состояние.</span><span class="sxs-lookup"><span data-stu-id="20faa-132">The ID of the task for which status is returned.</span></span>
- <span data-ttu-id="20faa-133">**TaskSteps**.</span><span class="sxs-lookup"><span data-stu-id="20faa-133">**TaskSteps**.</span></span>
<span data-ttu-id="20faa-134">**IList \<TaskStep\>**.</span><span class="sxs-lookup"><span data-stu-id="20faa-134">**IList\<TaskStep\>**.</span></span>
<span data-ttu-id="20faa-135">Каждый объект **TaskStep** имеет **подробные данные** , **ErrorCode** , **сообщение** , **результат** и **состояние**.</span><span class="sxs-lookup"><span data-stu-id="20faa-135">Each **TaskStep** object contains **Detail** , **ErrorCode** , **Message** , **Result** , and **Status**.</span></span>
- <span data-ttu-id="20faa-136">**Результат**.</span><span class="sxs-lookup"><span data-stu-id="20faa-136">**Result**.</span></span>
<span data-ttu-id="20faa-137">**TaskResult** , который включает общие результаты задачи.</span><span class="sxs-lookup"><span data-stu-id="20faa-137">**TaskResult** , which contains the overall result of the task.</span></span>
<span data-ttu-id="20faa-138">Допустимые значения: ошибка, успешно, PartialSuccess, отменено и недопустимо.</span><span class="sxs-lookup"><span data-stu-id="20faa-138">Valid values are: Failed, Succeeded, PartialSuccess, Cancelled, and Invalid.</span></span>
- <span data-ttu-id="20faa-139">**Состояние**.</span><span class="sxs-lookup"><span data-stu-id="20faa-139">**Status**.</span></span>
<span data-ttu-id="20faa-140">**TaskStatus** , который включает общее состояние выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="20faa-140">**TaskStatus** , which contains the overall running status of the task.</span></span>
<span data-ttu-id="20faa-141">Допустимые значения: "выполняется, недопустимо" и "завершено".</span><span class="sxs-lookup"><span data-stu-id="20faa-141">Valid values are: Inprogress, Invalid, and Completed.</span></span>
- <span data-ttu-id="20faa-142">**TaskResult**.</span><span class="sxs-lookup"><span data-stu-id="20faa-142">**TaskResult**.</span></span>
<span data-ttu-id="20faa-143">**TaskResult** — значение, вычисленное на основе **результата** и **состояния**.</span><span class="sxs-lookup"><span data-stu-id="20faa-143">**TaskResult** , a value computed based on **Result** and **Status**.</span></span>
<span data-ttu-id="20faa-144">Допустимые значения: ошибка, успешно, PartialSuccess, отмена и недопустимый.</span><span class="sxs-lookup"><span data-stu-id="20faa-144">Valid values are: Failed, Succeeded, InProgress, PartialSuccess, Cancelled, and Invalid.</span></span>

## <span data-ttu-id="20faa-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="20faa-145">NOTES</span></span>

## <span data-ttu-id="20faa-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="20faa-146">RELATED LINKS</span></span>

