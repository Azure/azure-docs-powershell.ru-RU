---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
ms.openlocfilehash: ea16c01e5c528742702dd08f1f2bd4c14e0cebcd
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399946"
---
# <span data-ttu-id="ff0ed-101">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="ff0ed-101">Get-AzNotificationHub</span></span>

## <span data-ttu-id="ff0ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff0ed-102">SYNOPSIS</span></span>
<span data-ttu-id="ff0ed-103">Получает сведения о концентраторах уведомлений.</span><span class="sxs-lookup"><span data-stu-id="ff0ed-103">Gets information about your notification hubs.</span></span>

## <span data-ttu-id="ff0ed-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ff0ed-104">SYNTAX</span></span>

```
Get-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff0ed-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff0ed-105">DESCRIPTION</span></span>
<span data-ttu-id="ff0ed-106">Чтобы получить сведения об **концентраторах** уведомлений в указанном пространстве имен и назначенную указанной группе ресурсов, можно получить сведения о концентраторах уведомлений.</span><span class="sxs-lookup"><span data-stu-id="ff0ed-106">The **Get-AzNotificationHub** cmdlet gets information about the notification hubs in a specified namespace and assigned to a specified resource group.</span></span>
<span data-ttu-id="ff0ed-107">Например, вы можете получить сведения для всех концентраторов уведомлений в области имен ContosoNamespace и на назначенную группу ресурсов ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="ff0ed-107">For example, you can get information for all the notification hubs in the namespace ContosoNamespace and assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="ff0ed-108">Кроме того, с помощью параметра *NotificationHub* можно ограничить возвращаемую информацию сведениями об определенном концентраторе уведомлений.</span><span class="sxs-lookup"><span data-stu-id="ff0ed-108">Alternatively, you can use the *NotificationHub* parameter to limit the returned data to information about a specific notification hub.</span></span>
<span data-ttu-id="ff0ed-109">Концентраторы уведомлений используются для отправки push-уведомлений нескольким клиентам независимо от платформы, например iOS, Android, Windows Phone 8 и Магазина Windows, которые используются этими клиентами.</span><span class="sxs-lookup"><span data-stu-id="ff0ed-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform, such as iOS, Android, Windows Phone 8, and Windows Store, used by those clients.</span></span>
<span data-ttu-id="ff0ed-110">Эти концентраторы примерно равны отдельным приложениям, и в каждом из них обычно есть собственный концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="ff0ed-110">These hubs are roughly equivalent to individual apps and each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="ff0ed-111">Этот cmdlet получает сведения только о самом центре.</span><span class="sxs-lookup"><span data-stu-id="ff0ed-111">This cmdlet only gets information about the hub itself.</span></span>
<span data-ttu-id="ff0ed-112">Другие cmdlets, такие как Get-AzNotificationHubAuthorizationRules, Get-AzNotificationHubListKeys и Get-AzNotificationHubPNSCredentials, необходимы для получения сведений о правилах авторизации концентратора, строках подключения и учетных данных службы уведомлений платформы.</span><span class="sxs-lookup"><span data-stu-id="ff0ed-112">Other cmdlets, such as Get-AzNotificationHubAuthorizationRules, Get-AzNotificationHubListKeys, and Get-AzNotificationHubPNSCredentials, are needed to get information about a hub's authorization rules, connection strings, and platform notification service credentials.</span></span>

## <span data-ttu-id="ff0ed-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ff0ed-113">EXAMPLES</span></span>

### <span data-ttu-id="ff0ed-114">Пример 1. Сведения для всех концентраторов уведомлений в определенном пространстве имен</span><span class="sxs-lookup"><span data-stu-id="ff0ed-114">Example 1: Get information for all notification hubs in a specific namespace</span></span>
```
PS C:\>Get-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="ff0ed-115">Эта команда получает сведения для всех концентраторов уведомлений в области имен ContosoNamespace, которые назначены группе ресурсов ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="ff0ed-115">This command gets information for all the notification hubs in the namespace named ContosoNamespace that have been assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="ff0ed-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff0ed-116">PARAMETERS</span></span>

### <span data-ttu-id="ff0ed-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff0ed-117">-DefaultProfile</span></span>
<span data-ttu-id="ff0ed-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ff0ed-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff0ed-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ff0ed-119">-Namespace</span></span>
<span data-ttu-id="ff0ed-120">Определяет пространство имен, которому назначен концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="ff0ed-120">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="ff0ed-121">Пространства имен предоставляют возможность группировать концентраторы уведомлений и классифицировать их.</span><span class="sxs-lookup"><span data-stu-id="ff0ed-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="ff0ed-122">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="ff0ed-122">-NotificationHub</span></span>
<span data-ttu-id="ff0ed-123">Указывает имя концентратора уведомлений, который получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff0ed-123">Specifies the name of the notification hub that this cmdlet gets.</span></span>
<span data-ttu-id="ff0ed-124">Концентраторы уведомлений используются для отправки push-уведомлений нескольким клиентам независимо от платформы, используемой этими клиентами.</span><span class="sxs-lookup"><span data-stu-id="ff0ed-124">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="ff0ed-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ff0ed-125">-ResourceGroup</span></span>
<span data-ttu-id="ff0ed-126">Группа ресурсов, которой назначен концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="ff0ed-126">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="ff0ed-127">Группы ресурсов упорядочиют такие элементы, как пространства имен, концентраторы уведомлений и правила авторизации, чтобы упрость управление запасами и администрирование Azure.</span><span class="sxs-lookup"><span data-stu-id="ff0ed-127">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="ff0ed-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff0ed-128">CommonParameters</span></span>
<span data-ttu-id="ff0ed-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff0ed-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff0ed-130">Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff0ed-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff0ed-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ff0ed-131">INPUTS</span></span>

### <span data-ttu-id="ff0ed-132">System.String</span><span class="sxs-lookup"><span data-stu-id="ff0ed-132">System.String</span></span>

## <span data-ttu-id="ff0ed-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ff0ed-133">OUTPUTS</span></span>

### <span data-ttu-id="ff0ed-134">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="ff0ed-134">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="ff0ed-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ff0ed-135">NOTES</span></span>

## <span data-ttu-id="ff0ed-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ff0ed-136">RELATED LINKS</span></span>




[<span data-ttu-id="ff0ed-137">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="ff0ed-137">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="ff0ed-138">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="ff0ed-138">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)

[<span data-ttu-id="ff0ed-139">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="ff0ed-139">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)


