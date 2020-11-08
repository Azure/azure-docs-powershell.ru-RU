---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
ms.openlocfilehash: 6fc2cfd47d9b03fc02d935245d1ec87d6831d173
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074507"
---
# <span data-ttu-id="6f3ea-101">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="6f3ea-101">Get-AzNotificationHub</span></span>

## <span data-ttu-id="6f3ea-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6f3ea-102">SYNOPSIS</span></span>
<span data-ttu-id="6f3ea-103">Получение сведений о концентраторах уведомлений.</span><span class="sxs-lookup"><span data-stu-id="6f3ea-103">Gets information about your notification hubs.</span></span>

## <span data-ttu-id="6f3ea-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6f3ea-104">SYNTAX</span></span>

```
Get-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f3ea-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f3ea-105">DESCRIPTION</span></span>
<span data-ttu-id="6f3ea-106">Командлет **Get-AzNotificationHub** получает сведения о концентраторах уведомлений в указанном пространстве имен и назначенных определенной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6f3ea-106">The **Get-AzNotificationHub** cmdlet gets information about the notification hubs in a specified namespace and assigned to a specified resource group.</span></span>
<span data-ttu-id="6f3ea-107">Например, вы можете получить сведения обо всех концентраторах уведомлений в пространстве имен ContosoNamespace и назначить группе ресурсов ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="6f3ea-107">For example, you can get information for all the notification hubs in the namespace ContosoNamespace and assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="6f3ea-108">Кроме того, можно использовать параметр *NotificationHub* для ограничения возвращенных данных сведениями об определенном концентраторе уведомлений.</span><span class="sxs-lookup"><span data-stu-id="6f3ea-108">Alternatively, you can use the *NotificationHub* parameter to limit the returned data to information about a specific notification hub.</span></span>
<span data-ttu-id="6f3ea-109">Концентраторы уведомлений используются для отправки push-уведомлений нескольким клиентам вне зависимости от платформы, например iOS, Android, Windows Phone 8 и магазина Windows, используемой этими клиентами.</span><span class="sxs-lookup"><span data-stu-id="6f3ea-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform, such as iOS, Android, Windows Phone 8, and Windows Store, used by those clients.</span></span>
<span data-ttu-id="6f3ea-110">Эти разветвители примерно эквивалентны отдельным приложениям, и каждое из ваших приложений обычно имеет собственный концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="6f3ea-110">These hubs are roughly equivalent to individual apps and each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="6f3ea-111">Этот командлет получает сведения только о самом концентраторе.</span><span class="sxs-lookup"><span data-stu-id="6f3ea-111">This cmdlet only gets information about the hub itself.</span></span>
<span data-ttu-id="6f3ea-112">Другие командлеты, такие как Get-AzNotificationHubAuthorizationRules, Get-AzNotificationHubListKeys и Get-AzNotificationHubPNSCredentials, необходимы для получения сведений о правилах авторизации концентратора, строках подключения и учетных данных службы уведомлений платформы.</span><span class="sxs-lookup"><span data-stu-id="6f3ea-112">Other cmdlets, such as Get-AzNotificationHubAuthorizationRules, Get-AzNotificationHubListKeys, and Get-AzNotificationHubPNSCredentials, are needed to get information about a hub's authorization rules, connection strings, and platform notification service credentials.</span></span>

## <span data-ttu-id="6f3ea-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6f3ea-113">EXAMPLES</span></span>

### <span data-ttu-id="6f3ea-114">Пример 1: получение сведений для всех концентраторов уведомлений в определенном пространстве имен</span><span class="sxs-lookup"><span data-stu-id="6f3ea-114">Example 1: Get information for all notification hubs in a specific namespace</span></span>
```
PS C:\>Get-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="6f3ea-115">Эта команда получает сведения для всех концентраторов уведомлений в пространстве имен с именем ContosoNamespace, назначенных группе ресурсов ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="6f3ea-115">This command gets information for all the notification hubs in the namespace named ContosoNamespace that have been assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="6f3ea-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6f3ea-116">PARAMETERS</span></span>

### <span data-ttu-id="6f3ea-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f3ea-117">-DefaultProfile</span></span>
<span data-ttu-id="6f3ea-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6f3ea-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f3ea-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6f3ea-119">-Namespace</span></span>
<span data-ttu-id="6f3ea-120">Задает пространство имен, которому назначен Центр уведомлений.</span><span class="sxs-lookup"><span data-stu-id="6f3ea-120">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="6f3ea-121">Пространства имен обеспечивают способ группировки и классификации концентраторов уведомлений.</span><span class="sxs-lookup"><span data-stu-id="6f3ea-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f3ea-122">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="6f3ea-122">-NotificationHub</span></span>
<span data-ttu-id="6f3ea-123">Указывает имя центра уведомлений, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="6f3ea-123">Specifies the name of the notification hub that this cmdlet gets.</span></span>
<span data-ttu-id="6f3ea-124">Концентраторы уведомлений используются для отправки push-уведомлений нескольким клиентам вне зависимости от платформы, используемой этими клиентами.</span><span class="sxs-lookup"><span data-stu-id="6f3ea-124">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f3ea-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6f3ea-125">-ResourceGroup</span></span>
<span data-ttu-id="6f3ea-126">Указывает группу ресурсов, которой назначен Центр уведомлений.</span><span class="sxs-lookup"><span data-stu-id="6f3ea-126">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="6f3ea-127">Группы ресурсов организуют элементы, такие как пространства имен, концентраторы уведомлений и правила авторизации, в целях простого управления запасами и администрирования Azure.</span><span class="sxs-lookup"><span data-stu-id="6f3ea-127">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f3ea-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f3ea-128">CommonParameters</span></span>
<span data-ttu-id="6f3ea-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6f3ea-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f3ea-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f3ea-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f3ea-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6f3ea-131">INPUTS</span></span>

### <span data-ttu-id="6f3ea-132">System. String</span><span class="sxs-lookup"><span data-stu-id="6f3ea-132">System.String</span></span>

## <span data-ttu-id="6f3ea-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f3ea-133">OUTPUTS</span></span>

### <span data-ttu-id="6f3ea-134">Microsoft. Azure. Commands. NotificationHubs. Models. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="6f3ea-134">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="6f3ea-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="6f3ea-135">NOTES</span></span>

## <span data-ttu-id="6f3ea-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6f3ea-136">RELATED LINKS</span></span>

[<span data-ttu-id="6f3ea-137">Get-AzNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="6f3ea-137">Get-AzNotificationHubAuthorizationRules</span></span>](./Get-AzNotificationHubAuthorizationRules.md)

[<span data-ttu-id="6f3ea-138">Get-AzNotificationHubListKeys</span><span class="sxs-lookup"><span data-stu-id="6f3ea-138">Get-AzNotificationHubListKeys</span></span>](./Get-AzNotificationHubListKeys.md)

[<span data-ttu-id="6f3ea-139">Get-AzNotificationHubPNSCredentials</span><span class="sxs-lookup"><span data-stu-id="6f3ea-139">Get-AzNotificationHubPNSCredentials</span></span>](./Get-AzNotificationHubPNSCredentials.md)

[<span data-ttu-id="6f3ea-140">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="6f3ea-140">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="6f3ea-141">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="6f3ea-141">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)

[<span data-ttu-id="6f3ea-142">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="6f3ea-142">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)


