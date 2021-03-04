---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/get-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
ms.openlocfilehash: fe2949e5b7eb8c3c5f1261072e755bcbb0b6eb00
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951416"
---
# <span data-ttu-id="7e3af-101">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="7e3af-101">Get-AzNotificationHub</span></span>

## <span data-ttu-id="7e3af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e3af-102">SYNOPSIS</span></span>
<span data-ttu-id="7e3af-103">Получает сведения о концентраторах уведомлений.</span><span class="sxs-lookup"><span data-stu-id="7e3af-103">Gets information about your notification hubs.</span></span>

## <span data-ttu-id="7e3af-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7e3af-104">SYNTAX</span></span>

```
Get-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e3af-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e3af-105">DESCRIPTION</span></span>
<span data-ttu-id="7e3af-106">Чтобы получить сведения об концентраторах уведомлений в указанном пространстве имен и назначенную указанной группе ресурсов, можно получить сведения о **cmdificationHub.**</span><span class="sxs-lookup"><span data-stu-id="7e3af-106">The **Get-AzNotificationHub** cmdlet gets information about the notification hubs in a specified namespace and assigned to a specified resource group.</span></span>
<span data-ttu-id="7e3af-107">Например, вы можете получить сведения для всех концентраторов уведомлений в области имен ContosoNamespace и на назначенную группу ресурсов ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="7e3af-107">For example, you can get information for all the notification hubs in the namespace ContosoNamespace and assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="7e3af-108">Кроме того, с помощью параметра *NotificationHub* можно ограничить возвращаемую информацию сведениями об определенном концентраторе уведомлений.</span><span class="sxs-lookup"><span data-stu-id="7e3af-108">Alternatively, you can use the *NotificationHub* parameter to limit the returned data to information about a specific notification hub.</span></span>
<span data-ttu-id="7e3af-109">Концентраторы уведомлений используются для отправки push-уведомлений нескольким клиентам независимо от платформы, например iOS, Android, Windows Phone 8 и Магазина Windows, которые используются этими клиентами.</span><span class="sxs-lookup"><span data-stu-id="7e3af-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform, such as iOS, Android, Windows Phone 8, and Windows Store, used by those clients.</span></span>
<span data-ttu-id="7e3af-110">Эти концентраторы примерно равны отдельным приложениям, и в каждом из них обычно есть собственный концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="7e3af-110">These hubs are roughly equivalent to individual apps and each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="7e3af-111">Этот cmdlet получает сведения только о самом центре.</span><span class="sxs-lookup"><span data-stu-id="7e3af-111">This cmdlet only gets information about the hub itself.</span></span>
<span data-ttu-id="7e3af-112">Другие cmdlets, такие как Get-AzNotificationHubAuthorizationRules, Get-AzNotificationHubListKeys и Get-AzNotificationHubPNSCredentials, необходимы для получения сведений о правилах авторизации концентратора, строках подключения и учетных данных службы уведомлений платформы.</span><span class="sxs-lookup"><span data-stu-id="7e3af-112">Other cmdlets, such as Get-AzNotificationHubAuthorizationRules, Get-AzNotificationHubListKeys, and Get-AzNotificationHubPNSCredentials, are needed to get information about a hub's authorization rules, connection strings, and platform notification service credentials.</span></span>

## <span data-ttu-id="7e3af-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7e3af-113">EXAMPLES</span></span>

### <span data-ttu-id="7e3af-114">Пример 1. Сведения для всех концентраторов уведомлений в определенном пространстве имен</span><span class="sxs-lookup"><span data-stu-id="7e3af-114">Example 1: Get information for all notification hubs in a specific namespace</span></span>
```powershell
PS C:\>Get-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="7e3af-115">Эта команда получает сведения для всех концентраторов уведомлений в области имен ContosoNamespace, которые назначены группе ресурсов ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="7e3af-115">This command gets information for all the notification hubs in the namespace named ContosoNamespace that have been assigned to the resource group ContosoNotificationsGroup.</span></span>

### <span data-ttu-id="7e3af-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="7e3af-116">Example 2</span></span>

<span data-ttu-id="7e3af-117">Получает сведения о концентраторах уведомлений.</span><span class="sxs-lookup"><span data-stu-id="7e3af-117">Gets information about your notification hubs.</span></span> <span data-ttu-id="7e3af-118">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="7e3af-118">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzNotificationHub -Namespace 'ContosoNamespace' -NotificationHub 'ContosoInternalHub' -ResourceGroup 'ContosoNotificationsGroup'
```

## <span data-ttu-id="7e3af-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e3af-119">PARAMETERS</span></span>

### <span data-ttu-id="7e3af-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e3af-120">-DefaultProfile</span></span>
<span data-ttu-id="7e3af-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7e3af-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e3af-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7e3af-122">-Namespace</span></span>
<span data-ttu-id="7e3af-123">Определяет пространство имен, которому назначен концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="7e3af-123">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="7e3af-124">Пространства имен предоставляют возможность группировать концентраторы уведомлений и классифицировать их.</span><span class="sxs-lookup"><span data-stu-id="7e3af-124">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="7e3af-125">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="7e3af-125">-NotificationHub</span></span>
<span data-ttu-id="7e3af-126">Указывает имя концентратора уведомлений, который получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e3af-126">Specifies the name of the notification hub that this cmdlet gets.</span></span>
<span data-ttu-id="7e3af-127">Концентраторы уведомлений используются для отправки push-уведомлений нескольким клиентам независимо от платформы, используемой этими клиентами.</span><span class="sxs-lookup"><span data-stu-id="7e3af-127">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="7e3af-128">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7e3af-128">-ResourceGroup</span></span>
<span data-ttu-id="7e3af-129">Группа ресурсов, которой назначен концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="7e3af-129">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="7e3af-130">Группы ресурсов упорядочиют такие элементы, как пространства имен, концентраторы уведомлений и правила авторизации, чтобы упрость управление запасами и администрирование Azure.</span><span class="sxs-lookup"><span data-stu-id="7e3af-130">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="7e3af-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e3af-131">CommonParameters</span></span>
<span data-ttu-id="7e3af-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e3af-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e3af-133">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e3af-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e3af-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7e3af-134">INPUTS</span></span>

### <span data-ttu-id="7e3af-135">System.String</span><span class="sxs-lookup"><span data-stu-id="7e3af-135">System.String</span></span>

## <span data-ttu-id="7e3af-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7e3af-136">OUTPUTS</span></span>

### <span data-ttu-id="7e3af-137">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="7e3af-137">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="7e3af-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7e3af-138">NOTES</span></span>

## <span data-ttu-id="7e3af-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7e3af-139">RELATED LINKS</span></span>

[<span data-ttu-id="7e3af-140">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7e3af-140">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="7e3af-141">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="7e3af-141">Get-AzNotificationHubListKey</span></span>](./Get-AzNotificationHubListKey.md)

[<span data-ttu-id="7e3af-142">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="7e3af-142">Get-AzNotificationHubPNSCredential</span></span>](./Get-AzNotificationHubPNSCredential.md)

[<span data-ttu-id="7e3af-143">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="7e3af-143">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="7e3af-144">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="7e3af-144">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)

[<span data-ttu-id="7e3af-145">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="7e3af-145">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)


