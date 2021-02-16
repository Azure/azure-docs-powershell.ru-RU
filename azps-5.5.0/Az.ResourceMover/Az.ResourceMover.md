---
Module Name: Az.ResourceMover
Module Guid: 97d87543-8eef-4574-a70d-7317ec4abe54
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
ms.openlocfilehash: b634b4e547b1e483037cec8efe5772b5460ee1b5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242616"
---
# <span data-ttu-id="2ad2a-101">Модуль Az.ResourceMover</span><span class="sxs-lookup"><span data-stu-id="2ad2a-101">Az.ResourceMover Module</span></span>
## <span data-ttu-id="2ad2a-102">Описание</span><span class="sxs-lookup"><span data-stu-id="2ad2a-102">Description</span></span>
<span data-ttu-id="2ad2a-103">Microsoft Azure PowerShell: cmdlets ResourceMover</span><span class="sxs-lookup"><span data-stu-id="2ad2a-103">Microsoft Azure PowerShell: ResourceMover cmdlets</span></span>

## <span data-ttu-id="2ad2a-104">Az.ResourceMover Cmdlets</span><span class="sxs-lookup"><span data-stu-id="2ad2a-104">Az.ResourceMover Cmdlets</span></span>
### [<span data-ttu-id="2ad2a-105">Add-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="2ad2a-105">Add-AzResourceMoverMoveResource</span></span>](Add-AzResourceMoverMoveResource.md)
<span data-ttu-id="2ad2a-106">Создает или обновляет перемещение ресурса в коллекции перемещения.</span><span class="sxs-lookup"><span data-stu-id="2ad2a-106">Creates or updates a Move Resource in the move collection.</span></span>

### [<span data-ttu-id="2ad2a-107">Get-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="2ad2a-107">Get-AzResourceMoverMoveCollection</span></span>](Get-AzResourceMoverMoveCollection.md)
<span data-ttu-id="2ad2a-108">Возвращает коллекцию перемещения.</span><span class="sxs-lookup"><span data-stu-id="2ad2a-108">Gets the move collection.</span></span>

### [<span data-ttu-id="2ad2a-109">Get-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="2ad2a-109">Get-AzResourceMoverMoveResource</span></span>](Get-AzResourceMoverMoveResource.md)
<span data-ttu-id="2ad2a-110">Возвращает ресурс перемещения.</span><span class="sxs-lookup"><span data-stu-id="2ad2a-110">Gets the Move Resource.</span></span>

### [<span data-ttu-id="2ad2a-111">Get-AzResourceMoverUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="2ad2a-111">Get-AzResourceMoverUnresolvedDependency</span></span>](Get-AzResourceMoverUnresolvedDependency.md)
<span data-ttu-id="2ad2a-112">Возвращает список разрешенных зависимостей.</span><span class="sxs-lookup"><span data-stu-id="2ad2a-112">Gets a list of unresolved dependencies.</span></span>

### [<span data-ttu-id="2ad2a-113">Invoke-AzResourceMoverCommit</span><span class="sxs-lookup"><span data-stu-id="2ad2a-113">Invoke-AzResourceMoverCommit</span></span>](Invoke-AzResourceMoverCommit.md)
<span data-ttu-id="2ad2a-114">Включает в себя набор ресурсов, включенных в запрос.</span><span class="sxs-lookup"><span data-stu-id="2ad2a-114">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="2ad2a-115">При успешном завершении перемещениеResources в moveState "CommitPending" или "CommitFailed" запускается для перемещенияResource moveState.</span><span class="sxs-lookup"><span data-stu-id="2ad2a-115">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="2ad2a-116">Чтобы помочь пользователю в предварительной проверке операции, клиент может позвонить, если для свойства validateOnly за установлено истинное имя.</span><span class="sxs-lookup"><span data-stu-id="2ad2a-116">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="2ad2a-117">Invoke-AzResourceMoverDiscard</span><span class="sxs-lookup"><span data-stu-id="2ad2a-117">Invoke-AzResourceMoverDiscard</span></span>](Invoke-AzResourceMoverDiscard.md)
<span data-ttu-id="2ad2a-118">Удаляет набор ресурсов, включенных в тело запроса.</span><span class="sxs-lookup"><span data-stu-id="2ad2a-118">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="2ad2a-119">При успешном завершении перемещениеResources в moveState "CommitPending" или "DiscardFailed" запускается операция отклонения moveResourceState.</span><span class="sxs-lookup"><span data-stu-id="2ad2a-119">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="2ad2a-120">Чтобы помочь пользователю в предварительной проверке операции, клиент может позвонить, если для свойства validateOnly за установлено истинное имя.</span><span class="sxs-lookup"><span data-stu-id="2ad2a-120">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="2ad2a-121">Invoke-AzResourceMoverInitiateMove</span><span class="sxs-lookup"><span data-stu-id="2ad2a-121">Invoke-AzResourceMoverInitiateMove</span></span>](Invoke-AzResourceMoverInitiateMove.md)
<span data-ttu-id="2ad2a-122">Перемещает набор ресурсов, включенных в запрос.</span><span class="sxs-lookup"><span data-stu-id="2ad2a-122">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="2ad2a-123">Операция перемещения запускается после перемещенияResources в moveState "MovePending" или "MoveFailed", при успешном завершении перемещениеResource MoveState сделает переход на CommitPending.</span><span class="sxs-lookup"><span data-stu-id="2ad2a-123">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="2ad2a-124">Чтобы помочь пользователю в предварительной проверке операции, клиент может позвонить, если для свойства validateOnly за установлено истинное имя.</span><span class="sxs-lookup"><span data-stu-id="2ad2a-124">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="2ad2a-125">Invoke-AzResourceMoverPrepare</span><span class="sxs-lookup"><span data-stu-id="2ad2a-125">Invoke-AzResourceMoverPrepare</span></span>](Invoke-AzResourceMoverPrepare.md)
<span data-ttu-id="2ad2a-126">Инициирует подготовку к набору ресурсов, включенных в запрос.</span><span class="sxs-lookup"><span data-stu-id="2ad2a-126">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="2ad2a-127">Операция подготовки находится на moveResources, которые находятся в moveState 'PreparePending' или 'PrepareFailed', при успешном завершении перемещениеResource MoveState сделает переход на MovePending.</span><span class="sxs-lookup"><span data-stu-id="2ad2a-127">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="2ad2a-128">Чтобы помочь пользователю в предварительной проверке операции, клиент может позвонить, если для свойства validateOnly за установлено истинное имя.</span><span class="sxs-lookup"><span data-stu-id="2ad2a-128">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

### [<span data-ttu-id="2ad2a-129">New-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="2ad2a-129">New-AzResourceMoverMoveCollection</span></span>](New-AzResourceMoverMoveCollection.md)
<span data-ttu-id="2ad2a-130">Создает или обновляет коллекцию перемещения.</span><span class="sxs-lookup"><span data-stu-id="2ad2a-130">Creates or updates a move collection.</span></span>

### [<span data-ttu-id="2ad2a-131">Remove-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="2ad2a-131">Remove-AzResourceMoverMoveCollection</span></span>](Remove-AzResourceMoverMoveCollection.md)
<span data-ttu-id="2ad2a-132">Удаляет коллекцию перемещения.</span><span class="sxs-lookup"><span data-stu-id="2ad2a-132">Deletes a move collection.</span></span>

### [<span data-ttu-id="2ad2a-133">Remove-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="2ad2a-133">Remove-AzResourceMoverMoveResource</span></span>](Remove-AzResourceMoverMoveResource.md)
<span data-ttu-id="2ad2a-134">Удаляет ресурс из коллекции перемещения.</span><span class="sxs-lookup"><span data-stu-id="2ad2a-134">Deletes a Move Resource from the move collection.</span></span>

### [<span data-ttu-id="2ad2a-135">Resolve-AzResourceMoverMoveCollectionDependency</span><span class="sxs-lookup"><span data-stu-id="2ad2a-135">Resolve-AzResourceMoverMoveCollectionDependency</span></span>](Resolve-AzResourceMoverMoveCollectionDependency.md)
<span data-ttu-id="2ad2a-136">Вычисляет, устраняет и проверяет зависимости moveResources в коллекции перемещения.</span><span class="sxs-lookup"><span data-stu-id="2ad2a-136">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

