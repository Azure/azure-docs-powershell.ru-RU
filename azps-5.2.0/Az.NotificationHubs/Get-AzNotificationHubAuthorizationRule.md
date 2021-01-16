---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 7A9D8F5A-6035-411B-8FDB-96ABFEED05A2
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 7c85bafabede1c905efaf000721e5f8d6bee1572
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395303"
---
# <span data-ttu-id="025bd-101">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="025bd-101">Get-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="025bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="025bd-102">SYNOPSIS</span></span>
<span data-ttu-id="025bd-103">Получает сведения о правилах авторизации, связанных с центром уведомлений.</span><span class="sxs-lookup"><span data-stu-id="025bd-103">Gets information about the authorization rules associated with a notification hub.</span></span>

## <span data-ttu-id="025bd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="025bd-104">SYNTAX</span></span>

```
Get-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="025bd-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="025bd-105">DESCRIPTION</span></span>
<span data-ttu-id="025bd-106">С **помощью cmdlet Get-AzNotificationHubAuthorizationRule** можно получить сведения о правилах авторизации saS, связанных с центром уведомлений.</span><span class="sxs-lookup"><span data-stu-id="025bd-106">The **Get-AzNotificationHubAuthorizationRule** cmdlet gets information about the Shared Access Signature (SAS) authorization rules associated with a notification hub.</span></span>
<span data-ttu-id="025bd-107">Он возвращает сведения обо всех правилах, связанных с центром, или, в том числе с параметром *AuthorizationRule,* получает сведения об определенном правиле.</span><span class="sxs-lookup"><span data-stu-id="025bd-107">The cmdlet returns information about all the rules associated with a hub or, by including the *AuthorizationRule* parameter, gets information about a specific rule.</span></span>
<span data-ttu-id="025bd-108">Правила авторизации управляют доступом к концентраторам уведомлений.</span><span class="sxs-lookup"><span data-stu-id="025bd-108">Authorization rules manage access to your notification hubs.</span></span>
<span data-ttu-id="025bd-109">Правило авторизации создает ссылки в качестве URI на основе различных уровней разрешений.</span><span class="sxs-lookup"><span data-stu-id="025bd-109">An authorization rule will create links, as a URI, based on different permission levels.</span></span>
<span data-ttu-id="025bd-110">Клиенты направляются на один из этих URL-адресов с учетом соответствующего уровня разрешений.</span><span class="sxs-lookup"><span data-stu-id="025bd-110">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="025bd-111">Например, клиент с разрешением "Прослушивание" будет направлен в URI для этого разрешения.</span><span class="sxs-lookup"><span data-stu-id="025bd-111">For instance, a client with the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="025bd-112">С **помощью cmdlet Get-AzNotificationHubAuthorizationRule** можно получить сведения только о правилах авторизации, связанных с центром уведомлений.</span><span class="sxs-lookup"><span data-stu-id="025bd-112">The **Get-AzNotificationHubAuthorizationRule** cmdlet only gets information about the authorization rules associated with a notification hub.</span></span>
<span data-ttu-id="025bd-113">Чтобы получить сведения о самом центре, используйте Get-AzNotificationHub.</span><span class="sxs-lookup"><span data-stu-id="025bd-113">To get information about the hub itself, use Get-AzNotificationHub.</span></span>

## <span data-ttu-id="025bd-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="025bd-114">EXAMPLES</span></span>

### <span data-ttu-id="025bd-115">Пример 1. Получите сведения для всех правил авторизации, которые назначены центру уведомлений</span><span class="sxs-lookup"><span data-stu-id="025bd-115">Example 1: Get information for all authorization rules assigned to a notification hub</span></span>
```
PS C:\>Get-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="025bd-116">Эта команда получает сведения для всех правил авторизации, которые назначены центру уведомлений ContosoInternalHub в области имен ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="025bd-116">This command gets information for all the authorization rules assigned to the notification hub named ContosoInternalHub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="025bd-117">Необходимо указать пространство имен, в котором находится центр, а также группу ресурсов, которой он назначен.</span><span class="sxs-lookup"><span data-stu-id="025bd-117">You must specify the namespace where the hub is located as well as the resource group that the hub has been assigned to.</span></span>

### <span data-ttu-id="025bd-118">Пример 2. Получите сведения о правилах авторизации, которые назначены центру уведомлений</span><span class="sxs-lookup"><span data-stu-id="025bd-118">Example 2: Get information for an authorization rules assigned to a notification hub</span></span>
```
PS C:\>Get-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="025bd-119">Эта команда получает сведения для всех правил авторизации, которые назначены центру уведомлений ContosoInternalHub в области имен ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="025bd-119">This command gets information for all the authorization rules assigned to the notification hub named ContosoInternalHub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="025bd-120">Команда использует параметр *AuthorizationRule,* чтобы ограничить возвращенные данные одним правилом авторизации с именем ListenRule.</span><span class="sxs-lookup"><span data-stu-id="025bd-120">The command uses the *AuthorizationRule* parameter to limit the returned data to a single authorization rule named ListenRule.</span></span>

## <span data-ttu-id="025bd-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="025bd-121">PARAMETERS</span></span>

### <span data-ttu-id="025bd-122">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="025bd-122">-AuthorizationRule</span></span>
<span data-ttu-id="025bd-123">Указывает имя правила проверки подлинности SAS.</span><span class="sxs-lookup"><span data-stu-id="025bd-123">Specifies the name of an SAS authentication rule.</span></span>
<span data-ttu-id="025bd-124">Эти правила определяют тип доступа пользователей к центру уведомлений.</span><span class="sxs-lookup"><span data-stu-id="025bd-124">These rules determine the type of access that users have to the notification hub.</span></span>

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

### <span data-ttu-id="025bd-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="025bd-125">-DefaultProfile</span></span>
<span data-ttu-id="025bd-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="025bd-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="025bd-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="025bd-127">-Namespace</span></span>
<span data-ttu-id="025bd-128">Определяет пространство имен, которому назначен концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="025bd-128">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="025bd-129">Пространства имен предоставляют возможность группировать и классифицировать концентраторы уведомлений.</span><span class="sxs-lookup"><span data-stu-id="025bd-129">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="025bd-130">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="025bd-130">-NotificationHub</span></span>
<span data-ttu-id="025bd-131">Указывает центр уведомлений, который этим cmdlet назначает правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="025bd-131">Specifies the notification hub that this cmdlet assigns authorization rules.</span></span>
<span data-ttu-id="025bd-132">Концентраторы уведомлений используются для отправки push-уведомлений нескольким клиентам независимо от платформы, используемой этими клиентами.</span><span class="sxs-lookup"><span data-stu-id="025bd-132">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="025bd-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="025bd-133">-ResourceGroup</span></span>
<span data-ttu-id="025bd-134">Группа ресурсов, которой назначен концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="025bd-134">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="025bd-135">Группы ресурсов упорядочиют такие элементы, как пространства имен, концентраторы уведомлений и правила авторизации, упрощая управление запасами и администрирование Azure.</span><span class="sxs-lookup"><span data-stu-id="025bd-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simplify inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="025bd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="025bd-136">CommonParameters</span></span>
<span data-ttu-id="025bd-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="025bd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="025bd-138">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="025bd-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="025bd-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="025bd-139">INPUTS</span></span>

### <span data-ttu-id="025bd-140">System.String</span><span class="sxs-lookup"><span data-stu-id="025bd-140">System.String</span></span>

## <span data-ttu-id="025bd-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="025bd-141">OUTPUTS</span></span>

### <span data-ttu-id="025bd-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="025bd-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="025bd-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="025bd-143">NOTES</span></span>

## <span data-ttu-id="025bd-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="025bd-144">RELATED LINKS</span></span>

[<span data-ttu-id="025bd-145">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="025bd-145">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="025bd-146">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="025bd-146">New-AzNotificationHubAuthorizationRule</span></span>](./New-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="025bd-147">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="025bd-147">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="025bd-148">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="025bd-148">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


