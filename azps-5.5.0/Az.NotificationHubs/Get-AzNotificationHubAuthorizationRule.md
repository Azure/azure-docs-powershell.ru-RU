---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 7A9D8F5A-6035-411B-8FDB-96ABFEED05A2
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 7c85bafabede1c905efaf000721e5f8d6bee1572
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100225601"
---
# <span data-ttu-id="f6d67-101">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f6d67-101">Get-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="f6d67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6d67-102">SYNOPSIS</span></span>
<span data-ttu-id="f6d67-103">Получает сведения о правилах авторизации, связанных с центром уведомлений.</span><span class="sxs-lookup"><span data-stu-id="f6d67-103">Gets information about the authorization rules associated with a notification hub.</span></span>

## <span data-ttu-id="f6d67-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f6d67-104">SYNTAX</span></span>

```
Get-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f6d67-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6d67-105">DESCRIPTION</span></span>
<span data-ttu-id="f6d67-106">С **помощью cmdlet Get-AzNotificationHubAuthorizationRule** можно получить сведения о правилах авторизации saS, связанных с центром уведомлений.</span><span class="sxs-lookup"><span data-stu-id="f6d67-106">The **Get-AzNotificationHubAuthorizationRule** cmdlet gets information about the Shared Access Signature (SAS) authorization rules associated with a notification hub.</span></span>
<span data-ttu-id="f6d67-107">Он возвращает сведения обо всех правилах, связанных с центром, или, в том числе с параметром *AuthorizationRule,* получает сведения об определенном правиле.</span><span class="sxs-lookup"><span data-stu-id="f6d67-107">The cmdlet returns information about all the rules associated with a hub or, by including the *AuthorizationRule* parameter, gets information about a specific rule.</span></span>
<span data-ttu-id="f6d67-108">Правила авторизации управляют доступом к концентраторам уведомлений.</span><span class="sxs-lookup"><span data-stu-id="f6d67-108">Authorization rules manage access to your notification hubs.</span></span>
<span data-ttu-id="f6d67-109">Правило авторизации создает ссылки в качестве URI на основе различных уровней разрешений.</span><span class="sxs-lookup"><span data-stu-id="f6d67-109">An authorization rule will create links, as a URI, based on different permission levels.</span></span>
<span data-ttu-id="f6d67-110">Клиенты направляются на один из этих URL-адресов с учетом соответствующего уровня разрешений.</span><span class="sxs-lookup"><span data-stu-id="f6d67-110">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="f6d67-111">Например, клиент с разрешением "Прослушивание" будет направлен в URI для этого разрешения.</span><span class="sxs-lookup"><span data-stu-id="f6d67-111">For instance, a client with the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="f6d67-112">С **помощью cmdlet Get-AzNotificationHubAuthorizationRule** можно получить сведения только о правилах авторизации, связанных с центром уведомлений.</span><span class="sxs-lookup"><span data-stu-id="f6d67-112">The **Get-AzNotificationHubAuthorizationRule** cmdlet only gets information about the authorization rules associated with a notification hub.</span></span>
<span data-ttu-id="f6d67-113">Чтобы получить сведения о самом центре, используйте Get-AzNotificationHub.</span><span class="sxs-lookup"><span data-stu-id="f6d67-113">To get information about the hub itself, use Get-AzNotificationHub.</span></span>

## <span data-ttu-id="f6d67-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f6d67-114">EXAMPLES</span></span>

### <span data-ttu-id="f6d67-115">Пример 1. Получите сведения для всех правил авторизации, которые назначены центру уведомлений</span><span class="sxs-lookup"><span data-stu-id="f6d67-115">Example 1: Get information for all authorization rules assigned to a notification hub</span></span>
```
PS C:\>Get-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="f6d67-116">Эта команда получает сведения для всех правил авторизации, которые назначены центру уведомлений ContosoInternalHub в области имен ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="f6d67-116">This command gets information for all the authorization rules assigned to the notification hub named ContosoInternalHub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="f6d67-117">Необходимо указать пространство имен, в котором находится центр, а также группу ресурсов, которой он назначен.</span><span class="sxs-lookup"><span data-stu-id="f6d67-117">You must specify the namespace where the hub is located as well as the resource group that the hub has been assigned to.</span></span>

### <span data-ttu-id="f6d67-118">Пример 2. Получите сведения о правилах авторизации, которые назначены центру уведомлений</span><span class="sxs-lookup"><span data-stu-id="f6d67-118">Example 2: Get information for an authorization rules assigned to a notification hub</span></span>
```
PS C:\>Get-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="f6d67-119">Эта команда получает сведения для всех правил авторизации, которые назначены центру уведомлений ContosoInternalHub в области имен ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="f6d67-119">This command gets information for all the authorization rules assigned to the notification hub named ContosoInternalHub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="f6d67-120">Команда использует параметр *AuthorizationRule,* чтобы ограничить возвращенные данные одним правилом авторизации с именем ListenRule.</span><span class="sxs-lookup"><span data-stu-id="f6d67-120">The command uses the *AuthorizationRule* parameter to limit the returned data to a single authorization rule named ListenRule.</span></span>

## <span data-ttu-id="f6d67-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f6d67-121">PARAMETERS</span></span>

### <span data-ttu-id="f6d67-122">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f6d67-122">-AuthorizationRule</span></span>
<span data-ttu-id="f6d67-123">Указывает имя правила проверки подлинности SAS.</span><span class="sxs-lookup"><span data-stu-id="f6d67-123">Specifies the name of an SAS authentication rule.</span></span>
<span data-ttu-id="f6d67-124">Эти правила определяют тип доступа пользователей к центру уведомлений.</span><span class="sxs-lookup"><span data-stu-id="f6d67-124">These rules determine the type of access that users have to the notification hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6d67-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6d67-125">-DefaultProfile</span></span>
<span data-ttu-id="f6d67-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f6d67-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f6d67-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f6d67-127">-Namespace</span></span>
<span data-ttu-id="f6d67-128">Определяет пространство имен, которому назначен концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="f6d67-128">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="f6d67-129">Пространства имен предоставляют возможность группировать концентраторы уведомлений и классифицировать их.</span><span class="sxs-lookup"><span data-stu-id="f6d67-129">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="f6d67-130">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="f6d67-130">-NotificationHub</span></span>
<span data-ttu-id="f6d67-131">Указывает центр уведомлений, который этим cmdlet назначает правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="f6d67-131">Specifies the notification hub that this cmdlet assigns authorization rules.</span></span>
<span data-ttu-id="f6d67-132">Концентраторы уведомлений используются для отправки push-уведомлений нескольким клиентам независимо от платформы, используемой этими клиентами.</span><span class="sxs-lookup"><span data-stu-id="f6d67-132">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6d67-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f6d67-133">-ResourceGroup</span></span>
<span data-ttu-id="f6d67-134">Группа ресурсов, которой назначен концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="f6d67-134">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="f6d67-135">Группы ресурсов упорядочиют такие элементы, как пространства имен, концентраторы уведомлений и правила авторизации, упрощая управление запасами и администрирование Azure.</span><span class="sxs-lookup"><span data-stu-id="f6d67-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simplify inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="f6d67-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6d67-136">CommonParameters</span></span>
<span data-ttu-id="f6d67-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6d67-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6d67-138">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6d67-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6d67-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f6d67-139">INPUTS</span></span>

### <span data-ttu-id="f6d67-140">System.String</span><span class="sxs-lookup"><span data-stu-id="f6d67-140">System.String</span></span>

## <span data-ttu-id="f6d67-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f6d67-141">OUTPUTS</span></span>

### <span data-ttu-id="f6d67-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="f6d67-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="f6d67-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f6d67-143">NOTES</span></span>

## <span data-ttu-id="f6d67-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f6d67-144">RELATED LINKS</span></span>

[<span data-ttu-id="f6d67-145">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f6d67-145">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="f6d67-146">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f6d67-146">New-AzNotificationHubAuthorizationRule</span></span>](./New-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="f6d67-147">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f6d67-147">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="f6d67-148">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f6d67-148">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


