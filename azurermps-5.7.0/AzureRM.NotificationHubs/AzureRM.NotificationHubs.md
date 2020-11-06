---
Module Name: AzureRM.NotificationHubs
Module Guid: f875725d-8ce4-423f-a6af-ea880bc63f13
Download Help Link:
  object Object: 
Help Version:
  object Object: 
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/AzureRM.NotificationHubs.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/AzureRM.NotificationHubs.md
ms.openlocfilehash: caab088ab796401cc9718da82118e3004d49ce45
ms.sourcegitcommit: d656467e32643b7bc9523e89a1360d92a171ff13
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/25/2019
ms.locfileid: "93555108"
---
# <span data-ttu-id="be8d1-101">Модуль AzureRM. NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="be8d1-101">AzureRM.NotificationHubs Module</span></span>
## <span data-ttu-id="be8d1-102">Nописание</span><span class="sxs-lookup"><span data-stu-id="be8d1-102">Description</span></span>
<span data-ttu-id="be8d1-103">В этом разделе отображаются разделы справки для командлетов центра уведомлений Azure.</span><span class="sxs-lookup"><span data-stu-id="be8d1-103">This topic displays help topics for the Azure Notification Hub cmdlets.</span></span> <span data-ttu-id="be8d1-104">Концентраторы уведомлений используются для отправки push-уведомлений нескольким клиентам вне зависимости от платформы (iOS, Android, Windows Phone 8, Магазин Windows и т. д.), используемых клиентами.</span><span class="sxs-lookup"><span data-stu-id="be8d1-104">Notification hubs are used to send push notifications to multiple clients regardless of the platform (iOS, Android, Windows Phone 8, Windows Store, etc.) used by those clients.</span></span> <span data-ttu-id="be8d1-105">Эти разветвители примерно эквивалентны отдельным приложениям: каждый из ваших приложений обычно имеет собственный концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="be8d1-105">These hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span> <span data-ttu-id="be8d1-106">Концентраторы уведомлений организованы в логических контейнерах (пространствах имен), а правила авторизации на доступ к ним используются для управления доступом к концентраторам и пространствам имен.</span><span class="sxs-lookup"><span data-stu-id="be8d1-106">Notification hubs are organized within logical containers known as namespaces, and Shared Access Signature (SAS) authorization rules are used to manage access to hubs and namespaces.</span></span> <span data-ttu-id="be8d1-107">Все эти элементы можно администрировать с помощью командлетов центра уведомлений.</span><span class="sxs-lookup"><span data-stu-id="be8d1-107">All of these elements can be administered by using the Notification Hub cmdlets.</span></span>

## <span data-ttu-id="be8d1-108">Командлеты AzureRM. NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="be8d1-108">AzureRM.NotificationHubs Cmdlets</span></span>
### [<span data-ttu-id="be8d1-109">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="be8d1-109">Get-AzureRmNotificationHub</span></span>](Get-AzureRmNotificationHub.md)
<span data-ttu-id="be8d1-110">Получение сведений о концентраторах уведомлений.</span><span class="sxs-lookup"><span data-stu-id="be8d1-110">Gets information about your notification hubs.</span></span>

### [<span data-ttu-id="be8d1-111">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="be8d1-111">Get-AzureRmNotificationHubAuthorizationRules</span></span>](Get-AzureRmNotificationHubAuthorizationRules.md)
<span data-ttu-id="be8d1-112">Получает сведения о правилах авторизации, связанных с центром уведомлений.</span><span class="sxs-lookup"><span data-stu-id="be8d1-112">Gets information about the authorization rules associated with a notification hub.</span></span>

### [<span data-ttu-id="be8d1-113">Get-AzureRmNotificationHubListKeys</span><span class="sxs-lookup"><span data-stu-id="be8d1-113">Get-AzureRmNotificationHubListKeys</span></span>](Get-AzureRmNotificationHubListKeys.md)
<span data-ttu-id="be8d1-114">Получает первичные и вторичные строки подключения, связанные с правилом авторизации концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="be8d1-114">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

### [<span data-ttu-id="be8d1-115">Get-AzureRmNotificationHubPNSCredentials</span><span class="sxs-lookup"><span data-stu-id="be8d1-115">Get-AzureRmNotificationHubPNSCredentials</span></span>](Get-AzureRmNotificationHubPNSCredentials.md)
<span data-ttu-id="be8d1-116">Возвращает учетные данные PNS для концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="be8d1-116">Gets the PNS credentials for a notification hub.</span></span>

### [<span data-ttu-id="be8d1-117">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="be8d1-117">Get-AzureRmNotificationHubsNamespace</span></span>](Get-AzureRmNotificationHubsNamespace.md)
<span data-ttu-id="be8d1-118">Получает сведения о пространстве имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="be8d1-118">Gets information about a notification hub namespace.</span></span>

### [<span data-ttu-id="be8d1-119">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="be8d1-119">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)
<span data-ttu-id="be8d1-120">Получает сведения о правилах авторизации, связанных с пространством имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="be8d1-120">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

### [<span data-ttu-id="be8d1-121">Get-AzureRmNotificationHubsNamespaceListKeys</span><span class="sxs-lookup"><span data-stu-id="be8d1-121">Get-AzureRmNotificationHubsNamespaceListKeys</span></span>](Get-AzureRmNotificationHubsNamespaceListKeys.md)
<span data-ttu-id="be8d1-122">Получает первичные и вторичные строки подключения, связанные с правилом авторизации пространства имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="be8d1-122">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

### [<span data-ttu-id="be8d1-123">New-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="be8d1-123">New-AzureRmNotificationHub</span></span>](New-AzureRmNotificationHub.md)
<span data-ttu-id="be8d1-124">Создает концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="be8d1-124">Creates a notification hub.</span></span>

### [<span data-ttu-id="be8d1-125">New-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="be8d1-125">New-AzureRmNotificationHubAuthorizationRules</span></span>](New-AzureRmNotificationHubAuthorizationRules.md)
<span data-ttu-id="be8d1-126">Создание правила авторизации и назначение правила для концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="be8d1-126">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

### [<span data-ttu-id="be8d1-127">New-AzureRmNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="be8d1-127">New-AzureRmNotificationHubKey</span></span>](New-AzureRmNotificationHubKey.md)
<span data-ttu-id="be8d1-128">Повторное создание ключа правила авторизации для NotificationHub.</span><span class="sxs-lookup"><span data-stu-id="be8d1-128">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

### [<span data-ttu-id="be8d1-129">New-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="be8d1-129">New-AzureRmNotificationHubsNamespace</span></span>](New-AzureRmNotificationHubsNamespace.md)
<span data-ttu-id="be8d1-130">Создает пространство имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="be8d1-130">Creates a notification hub namespace.</span></span>

### [<span data-ttu-id="be8d1-131">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="be8d1-131">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](New-AzureRmNotificationHubsNamespaceAuthorizationRules.md)
<span data-ttu-id="be8d1-132">Создает правило авторизации и назначает это правило пространству имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="be8d1-132">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

### [<span data-ttu-id="be8d1-133">New-AzureRmNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="be8d1-133">New-AzureRmNotificationHubsNamespaceKey</span></span>](New-AzureRmNotificationHubsNamespaceKey.md)
<span data-ttu-id="be8d1-134">Повторное создание ключа правила авторизации для пространства имен.</span><span class="sxs-lookup"><span data-stu-id="be8d1-134">Regenerate the Authorization Rule Key for a Namespace.</span></span>

### [<span data-ttu-id="be8d1-135">Remove-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="be8d1-135">Remove-AzureRmNotificationHub</span></span>](Remove-AzureRmNotificationHub.md)
<span data-ttu-id="be8d1-136">Удаляет существующий концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="be8d1-136">Removes an existing notification hub.</span></span>

### [<span data-ttu-id="be8d1-137">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="be8d1-137">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](Remove-AzureRmNotificationHubAuthorizationRules.md)
<span data-ttu-id="be8d1-138">Удаляет правило авторизации из концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="be8d1-138">Removes an authorization rule from a notification hub.</span></span>

### [<span data-ttu-id="be8d1-139">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="be8d1-139">Remove-AzureRmNotificationHubsNamespace</span></span>](Remove-AzureRmNotificationHubsNamespace.md)
<span data-ttu-id="be8d1-140">Удаляет пространство имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="be8d1-140">Removes a notification hub namespace.</span></span>

### [<span data-ttu-id="be8d1-141">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="be8d1-141">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](Remove-AzureRmNotificationHubsNamespaceAuthorizationRules.md)
<span data-ttu-id="be8d1-142">Удаляет правило авторизации из пространства имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="be8d1-142">Removes an authorization rule from a notification hub namespace.</span></span>

### [<span data-ttu-id="be8d1-143">Set-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="be8d1-143">Set-AzureRmNotificationHub</span></span>](Set-AzureRmNotificationHub.md)
<span data-ttu-id="be8d1-144">Задает значения свойств для центра уведомлений.</span><span class="sxs-lookup"><span data-stu-id="be8d1-144">Sets property values for a notification hub.</span></span>

### [<span data-ttu-id="be8d1-145">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="be8d1-145">Set-AzureRmNotificationHubAuthorizationRules</span></span>](Set-AzureRmNotificationHubAuthorizationRules.md)
<span data-ttu-id="be8d1-146">Задает правила авторизации для центра уведомлений.</span><span class="sxs-lookup"><span data-stu-id="be8d1-146">Sets authorization rules for a notification hub.</span></span>

### [<span data-ttu-id="be8d1-147">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="be8d1-147">Set-AzureRmNotificationHubsNamespace</span></span>](Set-AzureRmNotificationHubsNamespace.md)
<span data-ttu-id="be8d1-148">Задает значения свойств для пространства имен центра уведомлений.</span><span class="sxs-lookup"><span data-stu-id="be8d1-148">Sets property values for a notification hub namespace.</span></span>

### [<span data-ttu-id="be8d1-149">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="be8d1-149">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](Set-AzureRmNotificationHubsNamespaceAuthorizationRules.md)
<span data-ttu-id="be8d1-150">Задает правила авторизации для пространства имен центра уведомлений.</span><span class="sxs-lookup"><span data-stu-id="be8d1-150">Sets authorization rules for a notification hub namespace.</span></span>

