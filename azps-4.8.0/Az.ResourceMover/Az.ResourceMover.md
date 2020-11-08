---
Module Name: Az.ResourceMover
Module Guid: 97d87543-8eef-4574-a70d-7317ec4abe54
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
ms.openlocfilehash: b634b4e547b1e483037cec8efe5772b5460ee1b5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236418"
---
# <span data-ttu-id="80337-101">AZ. ResourceMover Module</span><span class="sxs-lookup"><span data-stu-id="80337-101">Az.ResourceMover Module</span></span>
## <span data-ttu-id="80337-102">Nописание</span><span class="sxs-lookup"><span data-stu-id="80337-102">Description</span></span>
<span data-ttu-id="80337-103">Командлеты Microsoft Azure PowerShell: ResourceMover</span><span class="sxs-lookup"><span data-stu-id="80337-103">Microsoft Azure PowerShell: ResourceMover cmdlets</span></span>

## <span data-ttu-id="80337-104">Командлеты AZ. ResourceMover</span><span class="sxs-lookup"><span data-stu-id="80337-104">Az.ResourceMover Cmdlets</span></span>
### [<span data-ttu-id="80337-105">Add-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="80337-105">Add-AzResourceMoverMoveResource</span></span>](Add-AzResourceMoverMoveResource.md)
<span data-ttu-id="80337-106">Создает или обновляет ресурс перемещения в коллекции Move.</span><span class="sxs-lookup"><span data-stu-id="80337-106">Creates or updates a Move Resource in the move collection.</span></span>

### [<span data-ttu-id="80337-107">Get-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="80337-107">Get-AzResourceMoverMoveCollection</span></span>](Get-AzResourceMoverMoveCollection.md)
<span data-ttu-id="80337-108">Получает коллекцию Move.</span><span class="sxs-lookup"><span data-stu-id="80337-108">Gets the move collection.</span></span>

### [<span data-ttu-id="80337-109">Get-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="80337-109">Get-AzResourceMoverMoveResource</span></span>](Get-AzResourceMoverMoveResource.md)
<span data-ttu-id="80337-110">Возвращает ресурс перемещения.</span><span class="sxs-lookup"><span data-stu-id="80337-110">Gets the Move Resource.</span></span>

### [<span data-ttu-id="80337-111">Get-AzResourceMoverUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="80337-111">Get-AzResourceMoverUnresolvedDependency</span></span>](Get-AzResourceMoverUnresolvedDependency.md)
<span data-ttu-id="80337-112">Получает список неразрешенных зависимостей.</span><span class="sxs-lookup"><span data-stu-id="80337-112">Gets a list of unresolved dependencies.</span></span>

### [<span data-ttu-id="80337-113">Invoke-AzResourceMoverCommit</span><span class="sxs-lookup"><span data-stu-id="80337-113">Invoke-AzResourceMoverCommit</span></span>](Invoke-AzResourceMoverCommit.md)
<span data-ttu-id="80337-114">Фиксирует набор ресурсов, включенных в текст запроса.</span><span class="sxs-lookup"><span data-stu-id="80337-114">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="80337-115">Операция Commit инициируется для moveResources в moveState "CommitPending" или "CommitFailed", после успешного завершения которого moveResource moveState выполняет переход на зафиксированный.</span><span class="sxs-lookup"><span data-stu-id="80337-115">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="80337-116">Чтобы помочь пользователю предварительно определить операцию, с помощью которой клиент может вызвать операцию, свойство validateOnly имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="80337-116">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="80337-117">Invoke-AzResourceMoverDiscard</span><span class="sxs-lookup"><span data-stu-id="80337-117">Invoke-AzResourceMoverDiscard</span></span>](Invoke-AzResourceMoverDiscard.md)
<span data-ttu-id="80337-118">Удаляет набор ресурсов, включенных в текст запроса.</span><span class="sxs-lookup"><span data-stu-id="80337-118">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="80337-119">Операция отмены вызывается для moveResources в moveState "CommitPending" или "DiscardFailed", после успешного завершения которого moveResource moveState выполняет переход к MovePending.</span><span class="sxs-lookup"><span data-stu-id="80337-119">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="80337-120">Чтобы помочь пользователю предварительно определить операцию, с помощью которой клиент может вызвать операцию, свойство validateOnly имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="80337-120">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="80337-121">Invoke-AzResourceMoverInitiateMove</span><span class="sxs-lookup"><span data-stu-id="80337-121">Invoke-AzResourceMoverInitiateMove</span></span>](Invoke-AzResourceMoverInitiateMove.md)
<span data-ttu-id="80337-122">Перемещает набор ресурсов, включенных в текст запроса.</span><span class="sxs-lookup"><span data-stu-id="80337-122">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="80337-123">Операция перемещения активируется после того, как moveResources находится в moveState "MovePending" или "MoveFailed", после успешного завершения moveResource moveState выполняет переход к CommitPending.</span><span class="sxs-lookup"><span data-stu-id="80337-123">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="80337-124">Чтобы помочь пользователю предварительно определить операцию, с помощью которой клиент может вызвать операцию, свойство validateOnly имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="80337-124">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="80337-125">Invoke-AzResourceMoverPrepare</span><span class="sxs-lookup"><span data-stu-id="80337-125">Invoke-AzResourceMoverPrepare</span></span>](Invoke-AzResourceMoverPrepare.md)
<span data-ttu-id="80337-126">Инициирует подготовку к набору ресурсов, включенных в текст запроса.</span><span class="sxs-lookup"><span data-stu-id="80337-126">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="80337-127">Операция подготовки находится на moveResources, которая находится в moveState "PreparePending" или "PrepareFailed", после успешного завершения moveResource moveState выполняет переход к MovePending.</span><span class="sxs-lookup"><span data-stu-id="80337-127">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="80337-128">Чтобы помочь пользователю предварительно определить операцию, с помощью которой клиент может вызвать операцию, свойство validateOnly имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="80337-128">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="80337-129">New-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="80337-129">New-AzResourceMoverMoveCollection</span></span>](New-AzResourceMoverMoveCollection.md)
<span data-ttu-id="80337-130">Создание или обновление коллекции перемещения.</span><span class="sxs-lookup"><span data-stu-id="80337-130">Creates or updates a move collection.</span></span>

### [<span data-ttu-id="80337-131">Remove-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="80337-131">Remove-AzResourceMoverMoveCollection</span></span>](Remove-AzResourceMoverMoveCollection.md)
<span data-ttu-id="80337-132">Удаляет коллекцию Move.</span><span class="sxs-lookup"><span data-stu-id="80337-132">Deletes a move collection.</span></span>

### [<span data-ttu-id="80337-133">Remove-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="80337-133">Remove-AzResourceMoverMoveResource</span></span>](Remove-AzResourceMoverMoveResource.md)
<span data-ttu-id="80337-134">Удаляет ресурс перемещения из коллекции Move.</span><span class="sxs-lookup"><span data-stu-id="80337-134">Deletes a Move Resource from the move collection.</span></span>

### [<span data-ttu-id="80337-135">Resolve-AzResourceMoverMoveCollectionDependency</span><span class="sxs-lookup"><span data-stu-id="80337-135">Resolve-AzResourceMoverMoveCollectionDependency</span></span>](Resolve-AzResourceMoverMoveCollectionDependency.md)
<span data-ttu-id="80337-136">Вычисляет, обрабатывает и проверяет зависимости moveResources в коллекции Move.</span><span class="sxs-lookup"><span data-stu-id="80337-136">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

