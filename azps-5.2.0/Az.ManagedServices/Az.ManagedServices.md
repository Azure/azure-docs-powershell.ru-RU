---
Module Name: Az.ManagedServices
Module Guid: fe0ae00c-c482-4e5f-a837-fbc342fdc7e0
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.managedservices
Help Version: 0.0.2
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
ms.openlocfilehash: 4b3d901b606e9ee8127d0ef47ea7847338a69a4c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415484"
---
# <span data-ttu-id="d1e75-101">Модуль Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="d1e75-101">Az.ManagedServices Module</span></span>
## <span data-ttu-id="d1e75-102">Описание</span><span class="sxs-lookup"><span data-stu-id="d1e75-102">Description</span></span>
<span data-ttu-id="d1e75-103">Эта функция используется клиентами управляемых поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="d1e75-103">This feature is used by customers of Managed Service Providers (MSPs).</span></span> <span data-ttu-id="d1e75-104">Клиенты могут предоставить MSP возможность управлять своей подпиской или группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d1e75-104">Customers give an MSP the ability to manage their subscription or resource group.</span></span> <span data-ttu-id="d1e75-105">Кроме предоставления доступа, клиент также может удалить или просмотреть существующий доступ.</span><span class="sxs-lookup"><span data-stu-id="d1e75-105">In addition to granting access, the customer can also remove access or view existing access.</span></span> <span data-ttu-id="d1e75-106">Они могут просматривать список клиентов, которые предоставили им доступ к подпискам.</span><span class="sxs-lookup"><span data-stu-id="d1e75-106">MSPs are able to view the list of customers who have granted them access to subscriptions.</span></span> <span data-ttu-id="d1e75-107">В этом процессе участвуют два объекта: определение регистрации, определяющее MSP и определения ролей, предоставленные пользователям MSP.</span><span class="sxs-lookup"><span data-stu-id="d1e75-107">There are two objects involved in this process: A registration definition which identifies the MSP and the role definitions granted to the MSP users.</span></span> <span data-ttu-id="d1e75-108">MSP может определить этот объект с помощью marketplace Managed Services, предлагая назначения Access, которые связывают подписку с определением.</span><span class="sxs-lookup"><span data-stu-id="d1e75-108">The MSP can optionally define this object using a Managed Services marketplace offering Access assignments which associate a subscription with the definition.</span></span>

## <span data-ttu-id="d1e75-109">Az.ManagedServices Cmdlets</span><span class="sxs-lookup"><span data-stu-id="d1e75-109">Az.ManagedServices Cmdlets</span></span>
### [<span data-ttu-id="d1e75-110">Get-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="d1e75-110">Get-AzManagedServicesAssignment</span></span>](Get-AzManagedServicesAssignment.md)
<span data-ttu-id="d1e75-111">Возвращает определенное назначение или список заданий по регистрации.</span><span class="sxs-lookup"><span data-stu-id="d1e75-111">Gets a specific registration assignment or a list of the registration assignments.</span></span>

### [<span data-ttu-id="d1e75-112">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="d1e75-112">Get-AzManagedServicesDefinition</span></span>](Get-AzManagedServicesDefinition.md)
<span data-ttu-id="d1e75-113">Получает определенное определение или список определений регистрации.</span><span class="sxs-lookup"><span data-stu-id="d1e75-113">Gets a specific registration definition or a list of the registration definitions.</span></span>

### [<span data-ttu-id="d1e75-114">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="d1e75-114">New-AzManagedServicesAssignment</span></span>](New-AzManagedServicesAssignment.md)
<span data-ttu-id="d1e75-115">Создает или обновляет назначение регистрации.</span><span class="sxs-lookup"><span data-stu-id="d1e75-115">Creates or updates a registration assignment.</span></span>

### [<span data-ttu-id="d1e75-116">New-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="d1e75-116">New-AzManagedServicesDefinition</span></span>](New-AzManagedServicesDefinition.md)
<span data-ttu-id="d1e75-117">Создание или обновление определения регистрации.</span><span class="sxs-lookup"><span data-stu-id="d1e75-117">Creates or updates a registration definition.</span></span>

### [<span data-ttu-id="d1e75-118">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="d1e75-118">Remove-AzManagedServicesAssignment</span></span>](Remove-AzManagedServicesAssignment.md)
<span data-ttu-id="d1e75-119">Удаление регистрационного назначения.</span><span class="sxs-lookup"><span data-stu-id="d1e75-119">Removes a registration assignment.</span></span>

### [<span data-ttu-id="d1e75-120">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="d1e75-120">Remove-AzManagedServicesDefinition</span></span>](Remove-AzManagedServicesDefinition.md)
<span data-ttu-id="d1e75-121">Удаляет определение регистрации.</span><span class="sxs-lookup"><span data-stu-id="d1e75-121">Removes a registration definition.</span></span>
