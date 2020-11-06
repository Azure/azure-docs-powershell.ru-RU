---
Module Name: AzureRM.Reservations
Module Guid: 43d3b085-6323-4ac4-a7c3-81d75ea036e5
Download Help Link: ''
Help Version: 1.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/AzureRM.Reservations.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/AzureRM.Reservations.md
ms.openlocfilehash: 10e22af397e5b5861eb9beb043e10abd04e08270
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "93554980"
---
# <span data-ttu-id="1ecfa-101">Модуль AzureRM. резервирования</span><span class="sxs-lookup"><span data-stu-id="1ecfa-101">AzureRM.Reservations Module</span></span>
## <span data-ttu-id="1ecfa-102">Nописание</span><span class="sxs-lookup"><span data-stu-id="1ecfa-102">Description</span></span>
<span data-ttu-id="1ecfa-103">В этом разделе приведены командлеты PowerShell Azure для резервирований Azure в платформе диспетчера ресурсов Azure (ARM).</span><span class="sxs-lookup"><span data-stu-id="1ecfa-103">The topics in this section document the Azure PowerShell cmdlets for Azure Reservations in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="1ecfa-104">Командлеты существуют в пространстве имен Microsoft. Azure. Commands. резервирования.</span><span class="sxs-lookup"><span data-stu-id="1ecfa-104">The cmdlets exist in the Microsoft.Azure.Commands.Reservations namespace.</span></span>

## <span data-ttu-id="1ecfa-105">Командлеты AzureRM. резервирования</span><span class="sxs-lookup"><span data-stu-id="1ecfa-105">AzureRM.Reservations Cmdlets</span></span>
### [<span data-ttu-id="1ecfa-106">Get-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="1ecfa-106">Get-AzureRmReservation</span></span>](Get-AzureRmReservation.md)
<span data-ttu-id="1ecfa-107">Получить `Reservation` s в заданном заказе на резервирование</span><span class="sxs-lookup"><span data-stu-id="1ecfa-107">Get `Reservation`s in a given reservation Order</span></span>

### [<span data-ttu-id="1ecfa-108">Get-AzureRmReservationCatalog</span><span class="sxs-lookup"><span data-stu-id="1ecfa-108">Get-AzureRmReservationCatalog</span></span>](Get-AzureRmReservationCatalog.md)
<span data-ttu-id="1ecfa-109">Получить доступ к каталогу свободного резервирования.</span><span class="sxs-lookup"><span data-stu-id="1ecfa-109">Get the catalog of available reservation.</span></span>

### [<span data-ttu-id="1ecfa-110">Get-AzureRmReservationHistory</span><span class="sxs-lookup"><span data-stu-id="1ecfa-110">Get-AzureRmReservationHistory</span></span>](Get-AzureRmReservationHistory.md)
<span data-ttu-id="1ecfa-111">Получение истории изменений для a `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="1ecfa-111">Get the revision history of a `Reservation`.</span></span>

### [<span data-ttu-id="1ecfa-112">Get-AzureRmReservationOrder</span><span class="sxs-lookup"><span data-stu-id="1ecfa-112">Get-AzureRmReservationOrder</span></span>](Get-AzureRmReservationOrder.md)
<span data-ttu-id="1ecfa-113">Получить `ReservationOrder` в разделе текущий клиент.</span><span class="sxs-lookup"><span data-stu-id="1ecfa-113">Get `ReservationOrder` under current tenant.</span></span> <span data-ttu-id="1ecfa-114">Если указан код заказа, извлекается определенный заказ.</span><span class="sxs-lookup"><span data-stu-id="1ecfa-114">If order id is provided, specific order is retrieved.</span></span>

### [<span data-ttu-id="1ecfa-115">Get-AzureRmReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="1ecfa-115">Get-AzureRmReservationOrderId</span></span>](Get-AzureRmReservationOrderId.md)
<span data-ttu-id="1ecfa-116">Получение списка приемлемых `ReservationOrder` идентификаторов для данной подписки.</span><span class="sxs-lookup"><span data-stu-id="1ecfa-116">Get list of applicable `ReservationOrder` Ids under given subscription.</span></span>

### [<span data-ttu-id="1ecfa-117">Merge-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="1ecfa-117">Merge-AzureRmReservation</span></span>](Merge-AzureRmReservation.md)
<span data-ttu-id="1ecfa-118">Объединение двух `Reservation` s в один `Reservation`</span><span class="sxs-lookup"><span data-stu-id="1ecfa-118">Merges two `Reservation`s into one `Reservation`</span></span>

### [<span data-ttu-id="1ecfa-119">Разделение — AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="1ecfa-119">Split-AzureRmReservation</span></span>](Split-AzureRmReservation.md)
<span data-ttu-id="1ecfa-120">Разделение на `Reservation` две `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="1ecfa-120">Split a `Reservation` into two `Reservation`s</span></span>

### [<span data-ttu-id="1ecfa-121">Update-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="1ecfa-121">Update-AzureRmReservation</span></span>](Update-AzureRmReservation.md)
<span data-ttu-id="1ecfa-122">Обновите примененную область для `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="1ecfa-122">Update the applied scope of a `Reservation`.</span></span>

