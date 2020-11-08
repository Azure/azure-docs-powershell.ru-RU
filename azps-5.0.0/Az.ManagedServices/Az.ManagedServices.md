---
Module Name: Az.ManagedServices
Module Guid: fe0ae00c-c482-4e5f-a837-fbc342fdc7e0
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.managedservices
Help Version: 0.0.2
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
ms.openlocfilehash: 4b3d901b606e9ee8127d0ef47ea7847338a69a4c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247692"
---
# <span data-ttu-id="f3762-101">AZ. ManagedServices Module</span><span class="sxs-lookup"><span data-stu-id="f3762-101">Az.ManagedServices Module</span></span>
## <span data-ttu-id="f3762-102">Nописание</span><span class="sxs-lookup"><span data-stu-id="f3762-102">Description</span></span>
<span data-ttu-id="f3762-103">Эта функция используется клиентами управляемых поставщиков услуг (MSPs).</span><span class="sxs-lookup"><span data-stu-id="f3762-103">This feature is used by customers of Managed Service Providers (MSPs).</span></span> <span data-ttu-id="f3762-104">Пользователи предоставляют MSP возможность управлять подпиской на подписку или группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f3762-104">Customers give an MSP the ability to manage their subscription or resource group.</span></span> <span data-ttu-id="f3762-105">В дополнение к предоставлению доступа клиент также может удалить доступ или просмотреть существующий доступ.</span><span class="sxs-lookup"><span data-stu-id="f3762-105">In addition to granting access, the customer can also remove access or view existing access.</span></span> <span data-ttu-id="f3762-106">MSPs смогут просмотреть список пользователей, которым предоставлен доступ к подпискам.</span><span class="sxs-lookup"><span data-stu-id="f3762-106">MSPs are able to view the list of customers who have granted them access to subscriptions.</span></span> <span data-ttu-id="f3762-107">Этот процесс включает в себя два объекта: определение регистрации, которое определяет MSP и определения ролей, предоставленные пользователям MSP.</span><span class="sxs-lookup"><span data-stu-id="f3762-107">There are two objects involved in this process: A registration definition which identifies the MSP and the role definitions granted to the MSP users.</span></span> <span data-ttu-id="f3762-108">MSP может дополнительно определять этот объект с помощью магазина управляемых служб, предлагающего назначения доступа, которые связывают подписку с определением.</span><span class="sxs-lookup"><span data-stu-id="f3762-108">The MSP can optionally define this object using a Managed Services marketplace offering Access assignments which associate a subscription with the definition.</span></span>

## <span data-ttu-id="f3762-109">Командлеты AZ. ManagedServices</span><span class="sxs-lookup"><span data-stu-id="f3762-109">Az.ManagedServices Cmdlets</span></span>
### [<span data-ttu-id="f3762-110">Get-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="f3762-110">Get-AzManagedServicesAssignment</span></span>](Get-AzManagedServicesAssignment.md)
<span data-ttu-id="f3762-111">Получает конкретное назначение регистрации или список назначений регистрации.</span><span class="sxs-lookup"><span data-stu-id="f3762-111">Gets a specific registration assignment or a list of the registration assignments.</span></span>

### [<span data-ttu-id="f3762-112">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="f3762-112">Get-AzManagedServicesDefinition</span></span>](Get-AzManagedServicesDefinition.md)
<span data-ttu-id="f3762-113">Возвращает определенную регистрационную запись или список определений регистрации.</span><span class="sxs-lookup"><span data-stu-id="f3762-113">Gets a specific registration definition or a list of the registration definitions.</span></span>

### [<span data-ttu-id="f3762-114">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="f3762-114">New-AzManagedServicesAssignment</span></span>](New-AzManagedServicesAssignment.md)
<span data-ttu-id="f3762-115">Создание или обновление назначения регистрации.</span><span class="sxs-lookup"><span data-stu-id="f3762-115">Creates or updates a registration assignment.</span></span>

### [<span data-ttu-id="f3762-116">New-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="f3762-116">New-AzManagedServicesDefinition</span></span>](New-AzManagedServicesDefinition.md)
<span data-ttu-id="f3762-117">Создание или обновление определения регистрации.</span><span class="sxs-lookup"><span data-stu-id="f3762-117">Creates or updates a registration definition.</span></span>

### [<span data-ttu-id="f3762-118">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="f3762-118">Remove-AzManagedServicesAssignment</span></span>](Remove-AzManagedServicesAssignment.md)
<span data-ttu-id="f3762-119">Удаление назначения регистрации.</span><span class="sxs-lookup"><span data-stu-id="f3762-119">Removes a registration assignment.</span></span>

### [<span data-ttu-id="f3762-120">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="f3762-120">Remove-AzManagedServicesDefinition</span></span>](Remove-AzManagedServicesDefinition.md)
<span data-ttu-id="f3762-121">Удаляет определение регистрации.</span><span class="sxs-lookup"><span data-stu-id="f3762-121">Removes a registration definition.</span></span>
