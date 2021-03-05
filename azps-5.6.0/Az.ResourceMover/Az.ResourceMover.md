---
Module Name: Az.ResourceMover
Module Guid: 97d87543-8eef-4574-a70d-7317ec4abe54
Download Help Link: https://docs.microsoft.com/powershell/module/az.resourcemover
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
ms.openlocfilehash: 0f43535baa284dbe9f7c69aee5a688443172089a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000051"
---
# <span data-ttu-id="3eabe-101">Модуль Az.ResourceMover</span><span class="sxs-lookup"><span data-stu-id="3eabe-101">Az.ResourceMover Module</span></span>
## <span data-ttu-id="3eabe-102">Описание</span><span class="sxs-lookup"><span data-stu-id="3eabe-102">Description</span></span>
<span data-ttu-id="3eabe-103">Microsoft Azure PowerShell: cmdlets ResourceMover</span><span class="sxs-lookup"><span data-stu-id="3eabe-103">Microsoft Azure PowerShell: ResourceMover cmdlets</span></span>

## <span data-ttu-id="3eabe-104">Az.ResourceMover Cmdlets</span><span class="sxs-lookup"><span data-stu-id="3eabe-104">Az.ResourceMover Cmdlets</span></span>
### [<span data-ttu-id="3eabe-105">Add-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="3eabe-105">Add-AzResourceMoverMoveResource</span></span>](Add-AzResourceMoverMoveResource.md)
<span data-ttu-id="3eabe-106">Создает или обновляет перемещение ресурса в коллекции перемещения.</span><span class="sxs-lookup"><span data-stu-id="3eabe-106">Creates or updates a Move Resource in the move collection.</span></span>

### [<span data-ttu-id="3eabe-107">Get-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="3eabe-107">Get-AzResourceMoverMoveCollection</span></span>](Get-AzResourceMoverMoveCollection.md)
<span data-ttu-id="3eabe-108">Возвращает коллекцию перемещения.</span><span class="sxs-lookup"><span data-stu-id="3eabe-108">Gets the move collection.</span></span>

### [<span data-ttu-id="3eabe-109">Get-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="3eabe-109">Get-AzResourceMoverMoveResource</span></span>](Get-AzResourceMoverMoveResource.md)
<span data-ttu-id="3eabe-110">Возвращает ресурс перемещения.</span><span class="sxs-lookup"><span data-stu-id="3eabe-110">Gets the Move Resource.</span></span>

### [<span data-ttu-id="3eabe-111">Get-AzResourceMoverRequiredForResources</span><span class="sxs-lookup"><span data-stu-id="3eabe-111">Get-AzResourceMoverRequiredForResources</span></span>](Get-AzResourceMoverRequiredForResources.md)
<span data-ttu-id="3eabe-112">Список ресурсов для перемещения, для которых требуется ресурс на arm.</span><span class="sxs-lookup"><span data-stu-id="3eabe-112">List of the move resources for which an arm resource is required for.</span></span>

### [<span data-ttu-id="3eabe-113">Get-AzResourceMoverUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="3eabe-113">Get-AzResourceMoverUnresolvedDependency</span></span>](Get-AzResourceMoverUnresolvedDependency.md)
<span data-ttu-id="3eabe-114">Возвращает список разрешенных зависимостей.</span><span class="sxs-lookup"><span data-stu-id="3eabe-114">Gets a list of unresolved dependencies.</span></span>

### [<span data-ttu-id="3eabe-115">Invoke-AzResourceMoverBulkRemove</span><span class="sxs-lookup"><span data-stu-id="3eabe-115">Invoke-AzResourceMoverBulkRemove</span></span>](Invoke-AzResourceMoverBulkRemove.md)
<span data-ttu-id="3eabe-116">Удаляет набор ресурсов перемещения, включенных в запрос, из коллекции.</span><span class="sxs-lookup"><span data-stu-id="3eabe-116">Removes the set of move resources included in the request body from move collection.</span></span>
<span data-ttu-id="3eabe-117">Развяжение будет сделано службой.</span><span class="sxs-lookup"><span data-stu-id="3eabe-117">The orchestration is done by service.</span></span>
<span data-ttu-id="3eabe-118">Чтобы помочь пользователю в предварительной проверке операции, клиент может позвонить, если для свойства validateOnly за установлено истинное имя.</span><span class="sxs-lookup"><span data-stu-id="3eabe-118">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="3eabe-119">Invoke-AzResourceMoverCommit</span><span class="sxs-lookup"><span data-stu-id="3eabe-119">Invoke-AzResourceMoverCommit</span></span>](Invoke-AzResourceMoverCommit.md)
<span data-ttu-id="3eabe-120">Включает в себя набор ресурсов, включенных в запрос.</span><span class="sxs-lookup"><span data-stu-id="3eabe-120">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="3eabe-121">При успешном завершении перемещениеResources в moveState "CommitPending" или "CommitFailed" запускается для перемещенияResource moveState.</span><span class="sxs-lookup"><span data-stu-id="3eabe-121">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="3eabe-122">Чтобы помочь пользователю в предварительной проверке операции, клиент может позвонить, если для свойства validateOnly за установлено истинное имя.</span><span class="sxs-lookup"><span data-stu-id="3eabe-122">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="3eabe-123">Invoke-AzResourceMoverDiscard</span><span class="sxs-lookup"><span data-stu-id="3eabe-123">Invoke-AzResourceMoverDiscard</span></span>](Invoke-AzResourceMoverDiscard.md)
<span data-ttu-id="3eabe-124">Удаляет набор ресурсов, включенных в тело запроса.</span><span class="sxs-lookup"><span data-stu-id="3eabe-124">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="3eabe-125">При успешном завершении перемещениеResources в moveState "CommitPending" или "DiscardFailed" запускается операция отклонения moveResourceState.</span><span class="sxs-lookup"><span data-stu-id="3eabe-125">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="3eabe-126">Чтобы помочь пользователю в предварительной проверке операции, клиент может позвонить, если для свойства validateOnly за установлено истинное имя.</span><span class="sxs-lookup"><span data-stu-id="3eabe-126">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="3eabe-127">Invoke-AzResourceMoverInitiateMove</span><span class="sxs-lookup"><span data-stu-id="3eabe-127">Invoke-AzResourceMoverInitiateMove</span></span>](Invoke-AzResourceMoverInitiateMove.md)
<span data-ttu-id="3eabe-128">Перемещает набор ресурсов, включенных в запрос.</span><span class="sxs-lookup"><span data-stu-id="3eabe-128">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="3eabe-129">Операция перемещения запускается после перемещенияResources в moveState "MovePending" или "MoveFailed", при успешном завершении перемещениеResource moveState сделает переход на CommitPending.</span><span class="sxs-lookup"><span data-stu-id="3eabe-129">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="3eabe-130">Чтобы помочь пользователю в предварительной проверке операции, клиент может позвонить, если для свойства validateOnly за установлено истинное имя.</span><span class="sxs-lookup"><span data-stu-id="3eabe-130">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="3eabe-131">Invoke-AzResourceMoverPrepare</span><span class="sxs-lookup"><span data-stu-id="3eabe-131">Invoke-AzResourceMoverPrepare</span></span>](Invoke-AzResourceMoverPrepare.md)
<span data-ttu-id="3eabe-132">Инициирует подготовку к набору ресурсов, включенных в запрос.</span><span class="sxs-lookup"><span data-stu-id="3eabe-132">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="3eabe-133">Операция подготовки находится на moveResources, которые находятся в moveState 'PreparePending' или 'PrepareFailed', при успешном завершении перемещениеResource MoveState сделает переход на MovePending.</span><span class="sxs-lookup"><span data-stu-id="3eabe-133">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="3eabe-134">Чтобы помочь пользователю в предварительной проверке операции, клиент может позвонить, если для свойства validateOnly за установлено истинное имя.</span><span class="sxs-lookup"><span data-stu-id="3eabe-134">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="3eabe-135">New-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="3eabe-135">New-AzResourceMoverMoveCollection</span></span>](New-AzResourceMoverMoveCollection.md)
<span data-ttu-id="3eabe-136">Создает или обновляет коллекцию перемещения.</span><span class="sxs-lookup"><span data-stu-id="3eabe-136">Creates or updates a move collection.</span></span>

### [<span data-ttu-id="3eabe-137">Remove-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="3eabe-137">Remove-AzResourceMoverMoveCollection</span></span>](Remove-AzResourceMoverMoveCollection.md)
<span data-ttu-id="3eabe-138">Удаляет коллекцию перемещения.</span><span class="sxs-lookup"><span data-stu-id="3eabe-138">Deletes a move collection.</span></span>

### [<span data-ttu-id="3eabe-139">Remove-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="3eabe-139">Remove-AzResourceMoverMoveResource</span></span>](Remove-AzResourceMoverMoveResource.md)
<span data-ttu-id="3eabe-140">Удаляет ресурс из коллекции перемещения.</span><span class="sxs-lookup"><span data-stu-id="3eabe-140">Deletes a Move Resource from the move collection.</span></span>

### [<span data-ttu-id="3eabe-141">Resolve-AzResourceMoverMoveCollectionDependency</span><span class="sxs-lookup"><span data-stu-id="3eabe-141">Resolve-AzResourceMoverMoveCollectionDependency</span></span>](Resolve-AzResourceMoverMoveCollectionDependency.md)
<span data-ttu-id="3eabe-142">Вычисляет, устраняет и проверяет зависимости moveResources в коллекции перемещения.</span><span class="sxs-lookup"><span data-stu-id="3eabe-142">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

