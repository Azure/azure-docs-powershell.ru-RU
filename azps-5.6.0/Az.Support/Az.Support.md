---
Module Name: Az.Support
Module Guid: 22d73af7-38c2-4bf6-b56f-4dc9db05d97a
Download Help Link: https://docs.microsoft.com/powershell/module/az.support
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
ms.openlocfilehash: b02401044f3b01a73954ac199cc15457cddb795a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979112"
---
# <span data-ttu-id="4b232-101">Модуль az.support</span><span class="sxs-lookup"><span data-stu-id="4b232-101">Az.Support Module</span></span>
## <span data-ttu-id="4b232-102">Описание</span><span class="sxs-lookup"><span data-stu-id="4b232-102">Description</span></span>
<span data-ttu-id="4b232-103">В разделах этой статьи ются командылеты Azure PowerShell для создания и управления входами в службу поддержки Azure в платформе Azure Resource Manager (ARM).</span><span class="sxs-lookup"><span data-stu-id="4b232-103">The topics in this section document the Azure PowerShell cmdlets for creating and managing Azure support tickets in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="4b232-104">Командлеты существуют в области имен Microsoft.Azure.Commands.Support.</span><span class="sxs-lookup"><span data-stu-id="4b232-104">The cmdlets exist in the Microsoft.Azure.Commands.Support namespace</span></span>

## <span data-ttu-id="4b232-105">Az.Support Cmdlets</span><span class="sxs-lookup"><span data-stu-id="4b232-105">Az.Support Cmdlets</span></span>
### [<span data-ttu-id="4b232-106">Get-AzSupportService</span><span class="sxs-lookup"><span data-stu-id="4b232-106">Get-AzSupportService</span></span>](Get-AzSupportService.md)
<span data-ttu-id="4b232-107">Возвращает текущий список служб Azure, для которых доступна поддержка.</span><span class="sxs-lookup"><span data-stu-id="4b232-107">Gets the current list of Azure services for which support is available.</span></span> <span data-ttu-id="4b232-108">Каждая служба Azure имеет собственный набор категорий, называемых классификацией проблем.</span><span class="sxs-lookup"><span data-stu-id="4b232-108">Each Azure service has its own set of categories called problem classification.</span></span> <span data-ttu-id="4b232-109">Получить текущий список классификации проблем для службы с помощью Get-AzSupportProblemClassification.</span><span class="sxs-lookup"><span data-stu-id="4b232-109">Get the current list of problem classification for a service using Get-AzSupportProblemClassification.</span></span> <span data-ttu-id="4b232-110">С помощью GUID классификации службы и проблемы можно создать новый билет в службу поддержки с помощью New-AzSupportTicket.</span><span class="sxs-lookup"><span data-stu-id="4b232-110">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span>

### [<span data-ttu-id="4b232-111">Get-AzSupportProblemClassification</span><span class="sxs-lookup"><span data-stu-id="4b232-111">Get-AzSupportProblemClassification</span></span>](Get-AzSupportProblemClassification.md)
<span data-ttu-id="4b232-112">Возвращает текущий список классификации проблем для службы Azure.</span><span class="sxs-lookup"><span data-stu-id="4b232-112">Gets the current list of problem classification for an Azure service.</span></span> <span data-ttu-id="4b232-113">С помощью GUID классификации службы и проблемы можно создать новый билет в службу поддержки с помощью New-AzSupportTicket.</span><span class="sxs-lookup"><span data-stu-id="4b232-113">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span> 

### [<span data-ttu-id="4b232-114">New-AzSupportContactProfileObject</span><span class="sxs-lookup"><span data-stu-id="4b232-114">New-AzSupportContactProfileObject</span></span>](New-AzSupportContactProfileObject.md)
<span data-ttu-id="4b232-115">Дополнительный cmdlet для создания объекта профиля контакта службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="4b232-115">Helper cmdlet to create a support contact profile object.</span></span> <span data-ttu-id="4b232-116">Этот объект можно использовать в New-AzSupportTicket.</span><span class="sxs-lookup"><span data-stu-id="4b232-116">You can use this object for New-AzSupportTicket cmdlet.</span></span>

### [<span data-ttu-id="4b232-117">New-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="4b232-117">New-AzSupportTicket</span></span>](New-AzSupportTicket.md)
<span data-ttu-id="4b232-118">Создает новый билет в службу поддержки Azure.</span><span class="sxs-lookup"><span data-stu-id="4b232-118">Creates a new Azure support ticket.</span></span> <span data-ttu-id="4b232-119">Эта операция смоделна с поведением страницы запроса на поддержку в Azure [New.](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview)</span><span class="sxs-lookup"><span data-stu-id="4b232-119">This operation is modeled on the behavior of the Azure [New support request page](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview).</span></span>

### [<span data-ttu-id="4b232-120">Get-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="4b232-120">Get-AzSupportTicket</span></span>](Get-AzSupportTicket.md)
<span data-ttu-id="4b232-121">Список билетов в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="4b232-121">Gets the list of support tickets.</span></span> <span data-ttu-id="4b232-122">Вы можете получить полные сведения о билете в службу поддержки по имени билета или отфильтровать его по status *или* *CreatedDate.*</span><span class="sxs-lookup"><span data-stu-id="4b232-122">You can get full support ticket details by ticket name or filter the support tickets by *Status* or *CreatedDate*.</span></span>

### [<span data-ttu-id="4b232-123">Update-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="4b232-123">Update-AzSupportTicket</span></span>](Update-AzSupportTicket.md)
<span data-ttu-id="4b232-124">Обновив уровень серьезности, статус или контактные данные клиента, обновив уровень обслуживания.</span><span class="sxs-lookup"><span data-stu-id="4b232-124">Update a support ticket's severity, status or customer contact details.</span></span>

### [<span data-ttu-id="4b232-125">Get-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="4b232-125">Get-AzSupportTicketCommunication</span></span>](Get-AzSupportTicketCommunication.md)
<span data-ttu-id="4b232-126">Получает сообщения для билета в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="4b232-126">Gets communications for a support ticket.</span></span> <span data-ttu-id="4b232-127">Вы также можете фильтровать сообщения о сообщениях в службу поддержки *по CreatedDate* или *CommunicationType.*</span><span class="sxs-lookup"><span data-stu-id="4b232-127">You can also filter support ticket communications by *CreatedDate* or *CommunicationType*.</span></span> 

### [<span data-ttu-id="4b232-128">New-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="4b232-128">New-AzSupportTicketCommunication</span></span>](New-AzSupportTicketCommunication.md)
<span data-ttu-id="4b232-129">Добавляет новое взаимодействие клиентов в билет в службу поддержки Azure.</span><span class="sxs-lookup"><span data-stu-id="4b232-129">Adds a new customer communication to an Azure support ticket.</span></span> 



