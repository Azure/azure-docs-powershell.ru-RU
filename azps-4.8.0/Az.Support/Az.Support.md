---
Module Name: Az.Support
Module Guid: 22d73af7-38c2-4bf6-b56f-4dc9db05d97a
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.support
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
ms.openlocfilehash: a662b6b405296b515d1b69c846775e5209a253dd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235711"
---
# <span data-ttu-id="862d7-101">AZ. Модуль поддержки</span><span class="sxs-lookup"><span data-stu-id="862d7-101">Az.Support Module</span></span>
## <span data-ttu-id="862d7-102">Nописание</span><span class="sxs-lookup"><span data-stu-id="862d7-102">Description</span></span>
<span data-ttu-id="862d7-103">В этом разделе приведены командлеты Azure PowerShell для создания билетов на службу поддержки Azure и управления ими в платформе диспетчера ресурсов Azure (ARM).</span><span class="sxs-lookup"><span data-stu-id="862d7-103">The topics in this section document the Azure PowerShell cmdlets for creating and managing Azure support tickets in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="862d7-104">Командлеты существуют в пространстве имен Microsoft. Azure. Commands. support</span><span class="sxs-lookup"><span data-stu-id="862d7-104">The cmdlets exist in the Microsoft.Azure.Commands.Support namespace</span></span>

## <span data-ttu-id="862d7-105">Поддержка командлетов AZ.</span><span class="sxs-lookup"><span data-stu-id="862d7-105">Az.Support Cmdlets</span></span>
### [<span data-ttu-id="862d7-106">Get-AzSupportService</span><span class="sxs-lookup"><span data-stu-id="862d7-106">Get-AzSupportService</span></span>](Get-AzSupportService.md)
<span data-ttu-id="862d7-107">Получает текущий список служб Azure, для которых доступна поддержка.</span><span class="sxs-lookup"><span data-stu-id="862d7-107">Gets the current list of Azure services for which support is available.</span></span> <span data-ttu-id="862d7-108">У каждой службы Azure есть собственный набор категорий с названием "Классификация проблем".</span><span class="sxs-lookup"><span data-stu-id="862d7-108">Each Azure service has its own set of categories called problem classification.</span></span> <span data-ttu-id="862d7-109">Получение текущего списка классификаций проблем для службы с помощью Get-AzSupportProblemClassification.</span><span class="sxs-lookup"><span data-stu-id="862d7-109">Get the current list of problem classification for a service using Get-AzSupportProblemClassification.</span></span> <span data-ttu-id="862d7-110">Для создания нового билета в службу поддержки с помощью New-AzSupportTicket можно использовать идентификатор GUID для классификации проблем и служб.</span><span class="sxs-lookup"><span data-stu-id="862d7-110">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span>

### [<span data-ttu-id="862d7-111">Get-AzSupportProblemClassification</span><span class="sxs-lookup"><span data-stu-id="862d7-111">Get-AzSupportProblemClassification</span></span>](Get-AzSupportProblemClassification.md)
<span data-ttu-id="862d7-112">Получает текущий список классификаций проблем для службы Azure.</span><span class="sxs-lookup"><span data-stu-id="862d7-112">Gets the current list of problem classification for an Azure service.</span></span> <span data-ttu-id="862d7-113">Для создания нового билета в службу поддержки с помощью New-AzSupportTicket можно использовать идентификатор GUID для классификации проблем и служб.</span><span class="sxs-lookup"><span data-stu-id="862d7-113">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span> 

### [<span data-ttu-id="862d7-114">New-AzSupportContactProfileObject</span><span class="sxs-lookup"><span data-stu-id="862d7-114">New-AzSupportContactProfileObject</span></span>](New-AzSupportContactProfileObject.md)
<span data-ttu-id="862d7-115">Вспомогательный командлет для создания объекта профиля контакта поддержки.</span><span class="sxs-lookup"><span data-stu-id="862d7-115">Helper cmdlet to create a support contact profile object.</span></span> <span data-ttu-id="862d7-116">Вы можете использовать этот объект для New-AzSupportTicket командлета.</span><span class="sxs-lookup"><span data-stu-id="862d7-116">You can use this object for New-AzSupportTicket cmdlet.</span></span>

### [<span data-ttu-id="862d7-117">New-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="862d7-117">New-AzSupportTicket</span></span>](New-AzSupportTicket.md)
<span data-ttu-id="862d7-118">Создание нового билета службы поддержки Azure.</span><span class="sxs-lookup"><span data-stu-id="862d7-118">Creates a new Azure support ticket.</span></span> <span data-ttu-id="862d7-119">Эта операция моделируется на [странице запроса новой поддержки](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview)Azure.</span><span class="sxs-lookup"><span data-stu-id="862d7-119">This operation is modeled on the behavior of the Azure [New support request page](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview).</span></span>

### [<span data-ttu-id="862d7-120">Get-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="862d7-120">Get-AzSupportTicket</span></span>](Get-AzSupportTicket.md)
<span data-ttu-id="862d7-121">Получает список билетов поддержки.</span><span class="sxs-lookup"><span data-stu-id="862d7-121">Gets the list of support tickets.</span></span> <span data-ttu-id="862d7-122">Вы можете получить сведения о билете на полную поддержку по имени билета или отфильтровать билеты поддержки по *состоянию* или *аргументы*.</span><span class="sxs-lookup"><span data-stu-id="862d7-122">You can get full support ticket details by ticket name or filter the support tickets by *Status* or *CreatedDate*.</span></span>

### [<span data-ttu-id="862d7-123">Update-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="862d7-123">Update-AzSupportTicket</span></span>](Update-AzSupportTicket.md)
<span data-ttu-id="862d7-124">Обновите сведения о серьезности билета в службу поддержки, его статус или контактные данные клиента.</span><span class="sxs-lookup"><span data-stu-id="862d7-124">Update a support ticket's severity, status or customer contact details.</span></span>

### [<span data-ttu-id="862d7-125">Get-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="862d7-125">Get-AzSupportTicketCommunication</span></span>](Get-AzSupportTicketCommunication.md)
<span data-ttu-id="862d7-126">Получает связь с билетом поддержки.</span><span class="sxs-lookup"><span data-stu-id="862d7-126">Gets communications for a support ticket.</span></span> <span data-ttu-id="862d7-127">Вы также можете отфильтровать билеты поддержки по *аргументы*   или *CommunicationType*.</span><span class="sxs-lookup"><span data-stu-id="862d7-127">You can also filter support ticket communications by *CreatedDate* or *CommunicationType*.</span></span> 

### [<span data-ttu-id="862d7-128">New-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="862d7-128">New-AzSupportTicketCommunication</span></span>](New-AzSupportTicketCommunication.md)
<span data-ttu-id="862d7-129">Добавляет новый клиентский связь с билетом службы поддержки Azure.</span><span class="sxs-lookup"><span data-stu-id="862d7-129">Adds a new customer communication to an Azure support ticket.</span></span> 



