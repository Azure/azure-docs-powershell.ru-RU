---
Module Name: Az.NotificationHubs
Module Guid: f875725d-8ce4-423f-a6af-ea880bc63f13
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs
Help Version: 4.1.1.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Az.NotificationHubs.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Az.NotificationHubs.md
ms.openlocfilehash: dd39a8f87120ea7aaddb4570276e1e3060873e2f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100213372"
---
# <span data-ttu-id="440bb-101">Модуль Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="440bb-101">Az.NotificationHubs Module</span></span>
## <span data-ttu-id="440bb-102">Описание</span><span class="sxs-lookup"><span data-stu-id="440bb-102">Description</span></span>
<span data-ttu-id="440bb-103">В этой теме отображаются разделы справки для концентраторов уведомлений Azure.</span><span class="sxs-lookup"><span data-stu-id="440bb-103">This topic displays help topics for the Azure Notification Hub cmdlets.</span></span> <span data-ttu-id="440bb-104">Концентраторы уведомлений используются для отправки push-уведомлений нескольким клиентам независимо от платформы (iOS, Android, Windows Phone 8, Магазина Windows и т. д.), используемой этими клиентами.</span><span class="sxs-lookup"><span data-stu-id="440bb-104">Notification hubs are used to send push notifications to multiple clients regardless of the platform (iOS, Android, Windows Phone 8, Windows Store, etc.) used by those clients.</span></span> <span data-ttu-id="440bb-105">Эти концентраторы примерно равны отдельным приложениям: в каждом из приложений обычно есть собственный концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="440bb-105">These hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span> <span data-ttu-id="440bb-106">Концентраторы уведомлений организованы в логических контейнерах, которые называются пространствами имен, а правила авторизации подписи общего доступа (SAS) используются для управления доступом к концентраторам и пространствам имен.</span><span class="sxs-lookup"><span data-stu-id="440bb-106">Notification hubs are organized within logical containers known as namespaces, and Shared Access Signature (SAS) authorization rules are used to manage access to hubs and namespaces.</span></span> <span data-ttu-id="440bb-107">Все эти элементы можно администрировать с помощью cmdlets Концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="440bb-107">All of these elements can be administered by using the Notification Hub cmdlets.</span></span>

## <span data-ttu-id="440bb-108">Az.NotificationHubs Cmdlets</span><span class="sxs-lookup"><span data-stu-id="440bb-108">Az.NotificationHubs Cmdlets</span></span>
### [<span data-ttu-id="440bb-109">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="440bb-109">Get-AzNotificationHub</span></span>](Get-AzNotificationHub.md)
<span data-ttu-id="440bb-110">Получает сведения о концентраторах уведомлений.</span><span class="sxs-lookup"><span data-stu-id="440bb-110">Gets information about your notification hubs.</span></span>

### [<span data-ttu-id="440bb-111">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="440bb-111">Get-AzNotificationHubAuthorizationRule</span></span>](Get-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="440bb-112">Получает сведения о правилах авторизации, связанных с центром уведомлений.</span><span class="sxs-lookup"><span data-stu-id="440bb-112">Gets information about the authorization rules associated with a notification hub.</span></span>

### [<span data-ttu-id="440bb-113">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="440bb-113">Get-AzNotificationHubListKey</span></span>](Get-AzNotificationHubListKey.md)
<span data-ttu-id="440bb-114">Возвращает основные и дополнительные строки подключения, связанные с правилом авторизации концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="440bb-114">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

### [<span data-ttu-id="440bb-115">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="440bb-115">Get-AzNotificationHubPNSCredential</span></span>](Get-AzNotificationHubPNSCredential.md)
<span data-ttu-id="440bb-116">Получает учетные данные PNS для концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="440bb-116">Gets the PNS credentials for a notification hub.</span></span>

### [<span data-ttu-id="440bb-117">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="440bb-117">Get-AzNotificationHubsNamespace</span></span>](Get-AzNotificationHubsNamespace.md)
<span data-ttu-id="440bb-118">Получает сведения о пространстве имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="440bb-118">Gets information about a notification hub namespace.</span></span>

### [<span data-ttu-id="440bb-119">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="440bb-119">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Get-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="440bb-120">Получает сведения о правилах авторизации, связанных с пространством имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="440bb-120">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

### [<span data-ttu-id="440bb-121">Get-AzNotificationHubsNamespaceListKey</span><span class="sxs-lookup"><span data-stu-id="440bb-121">Get-AzNotificationHubsNamespaceListKey</span></span>](Get-AzNotificationHubsNamespaceListKey.md)
<span data-ttu-id="440bb-122">Возвращает основные и дополнительные строки подключения, связанные с правилом авторизации пространства имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="440bb-122">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

### [<span data-ttu-id="440bb-123">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="440bb-123">New-AzNotificationHub</span></span>](New-AzNotificationHub.md)
<span data-ttu-id="440bb-124">Создает центр уведомлений.</span><span class="sxs-lookup"><span data-stu-id="440bb-124">Creates a notification hub.</span></span>

### [<span data-ttu-id="440bb-125">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="440bb-125">New-AzNotificationHubAuthorizationRule</span></span>](New-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="440bb-126">Создает правило авторизации и назначает его центру уведомлений.</span><span class="sxs-lookup"><span data-stu-id="440bb-126">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

### [<span data-ttu-id="440bb-127">New-AzNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="440bb-127">New-AzNotificationHubKey</span></span>](New-AzNotificationHubKey.md)
<span data-ttu-id="440bb-128">Повторно сгенерировать ключ правила авторизации для NotificationHub.</span><span class="sxs-lookup"><span data-stu-id="440bb-128">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

### [<span data-ttu-id="440bb-129">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="440bb-129">New-AzNotificationHubsNamespace</span></span>](New-AzNotificationHubsNamespace.md)
<span data-ttu-id="440bb-130">Создание пространства имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="440bb-130">Creates a notification hub namespace.</span></span>

### [<span data-ttu-id="440bb-131">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="440bb-131">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](New-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="440bb-132">Создает правило авторизации и назначает его области имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="440bb-132">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

### [<span data-ttu-id="440bb-133">New-AzNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="440bb-133">New-AzNotificationHubsNamespaceKey</span></span>](New-AzNotificationHubsNamespaceKey.md)
<span data-ttu-id="440bb-134">Повторно сгенерировать ключ правила авторизации для пространства имен.</span><span class="sxs-lookup"><span data-stu-id="440bb-134">Regenerate the Authorization Rule Key for a Namespace.</span></span>

### [<span data-ttu-id="440bb-135">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="440bb-135">Remove-AzNotificationHub</span></span>](Remove-AzNotificationHub.md)
<span data-ttu-id="440bb-136">Удаляет существующий концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="440bb-136">Removes an existing notification hub.</span></span>

### [<span data-ttu-id="440bb-137">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="440bb-137">Remove-AzNotificationHubAuthorizationRule</span></span>](Remove-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="440bb-138">Удаляет правило авторизации из концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="440bb-138">Removes an authorization rule from a notification hub.</span></span>

### [<span data-ttu-id="440bb-139">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="440bb-139">Remove-AzNotificationHubsNamespace</span></span>](Remove-AzNotificationHubsNamespace.md)
<span data-ttu-id="440bb-140">Удаляет пространство имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="440bb-140">Removes a notification hub namespace.</span></span>

### [<span data-ttu-id="440bb-141">Remove-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="440bb-141">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Remove-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="440bb-142">Удаляет правило авторизации из пространства имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="440bb-142">Removes an authorization rule from a notification hub namespace.</span></span>

### [<span data-ttu-id="440bb-143">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="440bb-143">Set-AzNotificationHub</span></span>](Set-AzNotificationHub.md)
<span data-ttu-id="440bb-144">Задает значения свойств для концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="440bb-144">Sets property values for a notification hub.</span></span>

### [<span data-ttu-id="440bb-145">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="440bb-145">Set-AzNotificationHubAuthorizationRule</span></span>](Set-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="440bb-146">Задает правила авторизации для концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="440bb-146">Sets authorization rules for a notification hub.</span></span>

### [<span data-ttu-id="440bb-147">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="440bb-147">Set-AzNotificationHubsNamespace</span></span>](Set-AzNotificationHubsNamespace.md)
<span data-ttu-id="440bb-148">Задает значения свойств для пространства имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="440bb-148">Sets property values for a notification hub namespace.</span></span>

### [<span data-ttu-id="440bb-149">Set-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="440bb-149">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Set-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="440bb-150">Задает правила авторизации для пространства имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="440bb-150">Sets authorization rules for a notification hub namespace.</span></span>

