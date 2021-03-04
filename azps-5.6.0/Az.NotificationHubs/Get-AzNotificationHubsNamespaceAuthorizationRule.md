---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/get-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: a1c9743d02f10102d9343709599dbed694d37a2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951299"
---
# <span data-ttu-id="7ff51-101">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7ff51-101">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="7ff51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ff51-102">SYNOPSIS</span></span>
<span data-ttu-id="7ff51-103">Получает сведения о правилах авторизации, связанных с пространством имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="7ff51-103">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

## <span data-ttu-id="7ff51-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7ff51-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ff51-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7ff51-105">DESCRIPTION</span></span>
<span data-ttu-id="7ff51-106">Cmdlet **Get-AzNotificationHubsNamespaceAuthorizationRule** возвращает сведения о правилах авторизации подписи общего доступа (SAS), связанных с пространством имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="7ff51-106">The **Get-AzNotificationHubsNamespaceAuthorizationRule** cmdlet returns information about the Shared Access Signature (SAS) authorization rules associated with a notification hub namespace.</span></span>
<span data-ttu-id="7ff51-107">Вы можете вернуть сведения обо всех правилах, связанных с пространством имен.</span><span class="sxs-lookup"><span data-stu-id="7ff51-107">You can return information about all the rules associated with the namespace.</span></span>
<span data-ttu-id="7ff51-108">Кроме того, с помощью параметра *AuthorizationRule* можно вернуть сведения для определенного правила.</span><span class="sxs-lookup"><span data-stu-id="7ff51-108">Alternatively, and by including the *AuthorizationRule* parameter, you can return information for a specific rule.</span></span>
<span data-ttu-id="7ff51-109">Правила авторизации управляют доступом к пространствам имен.</span><span class="sxs-lookup"><span data-stu-id="7ff51-109">Authorization rules manage access to namespaces.</span></span>
<span data-ttu-id="7ff51-110">Это делается путем создания ссылок ( URIS) на основе различных уровней разрешений.</span><span class="sxs-lookup"><span data-stu-id="7ff51-110">This is done through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="7ff51-111">Для платформы можно использовать один из следующих уровней:</span><span class="sxs-lookup"><span data-stu-id="7ff51-111">Platform levels can be one of the following:</span></span> 
- <span data-ttu-id="7ff51-112">Прослушивание</span><span class="sxs-lookup"><span data-stu-id="7ff51-112">Listen</span></span>
- <span data-ttu-id="7ff51-113">Отправить</span><span class="sxs-lookup"><span data-stu-id="7ff51-113">Send</span></span>
- <span data-ttu-id="7ff51-114">Управление клиентами направляется на один из этих URL-адресов с учетом соответствующего уровня разрешений.</span><span class="sxs-lookup"><span data-stu-id="7ff51-114">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="7ff51-115">Например, клиент с разрешением на прослушивание будет направлен в URI для этого разрешения.</span><span class="sxs-lookup"><span data-stu-id="7ff51-115">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="7ff51-116">Этот cmdlet получает только правила авторизации, связанные с пространством имен.</span><span class="sxs-lookup"><span data-stu-id="7ff51-116">This cmdlet only gets the authorization rules associated with a namespace.</span></span>
<span data-ttu-id="7ff51-117">Чтобы получить сведения о самом пространстве имен, используйте Get-AzNotificationHubsNamespace.</span><span class="sxs-lookup"><span data-stu-id="7ff51-117">To get information about the namespace itself, use Get-AzNotificationHubsNamespace.</span></span>

## <span data-ttu-id="7ff51-118">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7ff51-118">EXAMPLES</span></span>

### <span data-ttu-id="7ff51-119">Пример 1. Просмотр сведений обо всех правилах авторизации, которые назначены пространствам имен</span><span class="sxs-lookup"><span data-stu-id="7ff51-119">Example 1: Get information about all authorization rules assigned to namespaces</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="7ff51-120">Эта команда получает сведения обо всех правилах авторизации, которые назначены для пространства имен ContosoNamespace и группы ресурсов ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="7ff51-120">This command gets information about all the authorization rules assigned to both the namespace ContosoNamespace and the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="7ff51-121">Пример 2. Просмотр сведений о правиле авторизации</span><span class="sxs-lookup"><span data-stu-id="7ff51-121">Example 2: Get information about an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="7ff51-122">Эта команда получает сведения об одном правиле авторизации пространства имен с именем ListenRule.</span><span class="sxs-lookup"><span data-stu-id="7ff51-122">This command gets information about a single namespace authorization rule named ListenRule.</span></span>
<span data-ttu-id="7ff51-123">При получения сведений о конкретном правиле авторизации необходимо включить пространство имен и группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7ff51-123">You must include the namespace and the resource group when you get information for a specific authorization rule.</span></span>

## <span data-ttu-id="7ff51-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ff51-124">PARAMETERS</span></span>

### <span data-ttu-id="7ff51-125">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7ff51-125">-AuthorizationRule</span></span>
<span data-ttu-id="7ff51-126">Указывает имя правила проверки подлинности SAS.</span><span class="sxs-lookup"><span data-stu-id="7ff51-126">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="7ff51-127">Эти правила определяют тип доступа пользователей к области имен.</span><span class="sxs-lookup"><span data-stu-id="7ff51-127">These rules determine the type of access that users have to the namespace.</span></span>

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

### <span data-ttu-id="7ff51-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ff51-128">-DefaultProfile</span></span>
<span data-ttu-id="7ff51-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7ff51-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7ff51-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7ff51-130">-Namespace</span></span>
<span data-ttu-id="7ff51-131">Определяет пространство имен, которому назначены правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="7ff51-131">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="7ff51-132">Пространства имен предоставляют возможность группировать концентраторы уведомлений и классифицировать их.</span><span class="sxs-lookup"><span data-stu-id="7ff51-132">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="7ff51-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7ff51-133">-ResourceGroup</span></span>
<span data-ttu-id="7ff51-134">Группа ресурсов, которой назначены правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="7ff51-134">Specifies the resource group to which the authorization rules are assigned.</span></span>
<span data-ttu-id="7ff51-135">Группы ресурсов упорядочиют такие элементы, как пространства имен, концентраторы уведомлений и правила авторизации, чтобы упрость управление запасами и администрирование Azure.</span><span class="sxs-lookup"><span data-stu-id="7ff51-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="7ff51-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ff51-136">CommonParameters</span></span>
<span data-ttu-id="7ff51-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ff51-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ff51-138">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ff51-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ff51-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7ff51-139">INPUTS</span></span>

### <span data-ttu-id="7ff51-140">System.String</span><span class="sxs-lookup"><span data-stu-id="7ff51-140">System.String</span></span>

## <span data-ttu-id="7ff51-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7ff51-141">OUTPUTS</span></span>

### <span data-ttu-id="7ff51-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="7ff51-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="7ff51-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7ff51-143">NOTES</span></span>

## <span data-ttu-id="7ff51-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7ff51-144">RELATED LINKS</span></span>

[<span data-ttu-id="7ff51-145">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="7ff51-145">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="7ff51-146">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="7ff51-146">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="7ff51-147">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="7ff51-147">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)

[<span data-ttu-id="7ff51-148">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="7ff51-148">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


