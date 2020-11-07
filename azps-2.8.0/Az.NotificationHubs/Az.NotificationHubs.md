---
Module Name: Az.NotificationHubs
Module Guid: f875725d-8ce4-423f-a6af-ea880bc63f13
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs
Help Version: 4.1.1.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Az.NotificationHubs.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Az.NotificationHubs.md
ms.openlocfilehash: dd39a8f87120ea7aaddb4570276e1e3060873e2f
ms.sourcegitcommit: 0b94b9566124331d0b15eb7f5a811305c254172e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/15/2019
ms.locfileid: "93720050"
---
# <span data-ttu-id="3f327-101">AZ. NotificationHubs Module</span><span class="sxs-lookup"><span data-stu-id="3f327-101">Az.NotificationHubs Module</span></span>
## <span data-ttu-id="3f327-102">Nописание</span><span class="sxs-lookup"><span data-stu-id="3f327-102">Description</span></span>
<span data-ttu-id="3f327-103">В этом разделе отображаются разделы справки для командлетов центра уведомлений Azure.</span><span class="sxs-lookup"><span data-stu-id="3f327-103">This topic displays help topics for the Azure Notification Hub cmdlets.</span></span> <span data-ttu-id="3f327-104">Концентраторы уведомлений используются для отправки push-уведомлений нескольким клиентам вне зависимости от платформы (iOS, Android, Windows Phone 8, Магазин Windows и т. д.), используемых клиентами.</span><span class="sxs-lookup"><span data-stu-id="3f327-104">Notification hubs are used to send push notifications to multiple clients regardless of the platform (iOS, Android, Windows Phone 8, Windows Store, etc.) used by those clients.</span></span> <span data-ttu-id="3f327-105">Эти разветвители примерно эквивалентны отдельным приложениям: каждый из ваших приложений обычно имеет собственный концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3f327-105">These hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span> <span data-ttu-id="3f327-106">Концентраторы уведомлений организованы в логических контейнерах (пространствах имен), а правила авторизации на доступ к ним используются для управления доступом к концентраторам и пространствам имен.</span><span class="sxs-lookup"><span data-stu-id="3f327-106">Notification hubs are organized within logical containers known as namespaces, and Shared Access Signature (SAS) authorization rules are used to manage access to hubs and namespaces.</span></span> <span data-ttu-id="3f327-107">Все эти элементы можно администрировать с помощью командлетов центра уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3f327-107">All of these elements can be administered by using the Notification Hub cmdlets.</span></span>

## <span data-ttu-id="3f327-108">Командлеты AZ. NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="3f327-108">Az.NotificationHubs Cmdlets</span></span>
### [<span data-ttu-id="3f327-109">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="3f327-109">Get-AzNotificationHub</span></span>](Get-AzNotificationHub.md)
<span data-ttu-id="3f327-110">Получение сведений о концентраторах уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3f327-110">Gets information about your notification hubs.</span></span>

### [<span data-ttu-id="3f327-111">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3f327-111">Get-AzNotificationHubAuthorizationRule</span></span>](Get-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="3f327-112">Получает сведения о правилах авторизации, связанных с центром уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3f327-112">Gets information about the authorization rules associated with a notification hub.</span></span>

### [<span data-ttu-id="3f327-113">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="3f327-113">Get-AzNotificationHubListKey</span></span>](Get-AzNotificationHubListKey.md)
<span data-ttu-id="3f327-114">Получает первичные и вторичные строки подключения, связанные с правилом авторизации концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3f327-114">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

### [<span data-ttu-id="3f327-115">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="3f327-115">Get-AzNotificationHubPNSCredential</span></span>](Get-AzNotificationHubPNSCredential.md)
<span data-ttu-id="3f327-116">Возвращает учетные данные PNS для концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3f327-116">Gets the PNS credentials for a notification hub.</span></span>

### [<span data-ttu-id="3f327-117">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="3f327-117">Get-AzNotificationHubsNamespace</span></span>](Get-AzNotificationHubsNamespace.md)
<span data-ttu-id="3f327-118">Получает сведения о пространстве имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3f327-118">Gets information about a notification hub namespace.</span></span>

### [<span data-ttu-id="3f327-119">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3f327-119">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Get-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="3f327-120">Получает сведения о правилах авторизации, связанных с пространством имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3f327-120">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

### [<span data-ttu-id="3f327-121">Get-AzNotificationHubsNamespaceListKey</span><span class="sxs-lookup"><span data-stu-id="3f327-121">Get-AzNotificationHubsNamespaceListKey</span></span>](Get-AzNotificationHubsNamespaceListKey.md)
<span data-ttu-id="3f327-122">Получает первичные и вторичные строки подключения, связанные с правилом авторизации пространства имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3f327-122">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

### [<span data-ttu-id="3f327-123">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="3f327-123">New-AzNotificationHub</span></span>](New-AzNotificationHub.md)
<span data-ttu-id="3f327-124">Создает концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3f327-124">Creates a notification hub.</span></span>

### [<span data-ttu-id="3f327-125">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3f327-125">New-AzNotificationHubAuthorizationRule</span></span>](New-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="3f327-126">Создание правила авторизации и назначение правила для концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3f327-126">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

### [<span data-ttu-id="3f327-127">New-AzNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="3f327-127">New-AzNotificationHubKey</span></span>](New-AzNotificationHubKey.md)
<span data-ttu-id="3f327-128">Повторное создание ключа правила авторизации для NotificationHub.</span><span class="sxs-lookup"><span data-stu-id="3f327-128">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

### [<span data-ttu-id="3f327-129">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="3f327-129">New-AzNotificationHubsNamespace</span></span>](New-AzNotificationHubsNamespace.md)
<span data-ttu-id="3f327-130">Создает пространство имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3f327-130">Creates a notification hub namespace.</span></span>

### [<span data-ttu-id="3f327-131">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3f327-131">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](New-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="3f327-132">Создает правило авторизации и назначает это правило пространству имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3f327-132">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

### [<span data-ttu-id="3f327-133">New-AzNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="3f327-133">New-AzNotificationHubsNamespaceKey</span></span>](New-AzNotificationHubsNamespaceKey.md)
<span data-ttu-id="3f327-134">Повторное создание ключа правила авторизации для пространства имен.</span><span class="sxs-lookup"><span data-stu-id="3f327-134">Regenerate the Authorization Rule Key for a Namespace.</span></span>

### [<span data-ttu-id="3f327-135">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="3f327-135">Remove-AzNotificationHub</span></span>](Remove-AzNotificationHub.md)
<span data-ttu-id="3f327-136">Удаляет существующий концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3f327-136">Removes an existing notification hub.</span></span>

### [<span data-ttu-id="3f327-137">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3f327-137">Remove-AzNotificationHubAuthorizationRule</span></span>](Remove-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="3f327-138">Удаляет правило авторизации из концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3f327-138">Removes an authorization rule from a notification hub.</span></span>

### [<span data-ttu-id="3f327-139">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="3f327-139">Remove-AzNotificationHubsNamespace</span></span>](Remove-AzNotificationHubsNamespace.md)
<span data-ttu-id="3f327-140">Удаляет пространство имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3f327-140">Removes a notification hub namespace.</span></span>

### [<span data-ttu-id="3f327-141">Remove-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3f327-141">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Remove-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="3f327-142">Удаляет правило авторизации из пространства имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3f327-142">Removes an authorization rule from a notification hub namespace.</span></span>

### [<span data-ttu-id="3f327-143">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="3f327-143">Set-AzNotificationHub</span></span>](Set-AzNotificationHub.md)
<span data-ttu-id="3f327-144">Задает значения свойств для центра уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3f327-144">Sets property values for a notification hub.</span></span>

### [<span data-ttu-id="3f327-145">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3f327-145">Set-AzNotificationHubAuthorizationRule</span></span>](Set-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="3f327-146">Задает правила авторизации для центра уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3f327-146">Sets authorization rules for a notification hub.</span></span>

### [<span data-ttu-id="3f327-147">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="3f327-147">Set-AzNotificationHubsNamespace</span></span>](Set-AzNotificationHubsNamespace.md)
<span data-ttu-id="3f327-148">Задает значения свойств для пространства имен центра уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3f327-148">Sets property values for a notification hub namespace.</span></span>

### [<span data-ttu-id="3f327-149">Set-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3f327-149">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Set-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="3f327-150">Задает правила авторизации для пространства имен центра уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3f327-150">Sets authorization rules for a notification hub namespace.</span></span>

