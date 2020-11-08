---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 7A9D8F5A-6035-411B-8FDB-96ABFEED05A2
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 7c85bafabede1c905efaf000721e5f8d6bee1572
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074504"
---
# <span data-ttu-id="f7c6a-101">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f7c6a-101">Get-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="f7c6a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f7c6a-102">SYNOPSIS</span></span>
<span data-ttu-id="f7c6a-103">Получает сведения о правилах авторизации, связанных с центром уведомлений.</span><span class="sxs-lookup"><span data-stu-id="f7c6a-103">Gets information about the authorization rules associated with a notification hub.</span></span>

## <span data-ttu-id="f7c6a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f7c6a-104">SYNTAX</span></span>

```
Get-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f7c6a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7c6a-105">DESCRIPTION</span></span>
<span data-ttu-id="f7c6a-106">Командлет **Get-AzNotificationHubAuthorizationRule** получает сведения о правилах авторизации для общих подписей доступа (SAS), связанных с центром уведомлений.</span><span class="sxs-lookup"><span data-stu-id="f7c6a-106">The **Get-AzNotificationHubAuthorizationRule** cmdlet gets information about the Shared Access Signature (SAS) authorization rules associated with a notification hub.</span></span>
<span data-ttu-id="f7c6a-107">Командлет возвращает сведения о конкретном правиле, а также о всех правилах, связанных с основным приложением или с помощью параметра *AuthorizationRule* .</span><span class="sxs-lookup"><span data-stu-id="f7c6a-107">The cmdlet returns information about all the rules associated with a hub or, by including the *AuthorizationRule* parameter, gets information about a specific rule.</span></span>
<span data-ttu-id="f7c6a-108">Правила авторизации управляют доступом к концентраторам уведомлений.</span><span class="sxs-lookup"><span data-stu-id="f7c6a-108">Authorization rules manage access to your notification hubs.</span></span>
<span data-ttu-id="f7c6a-109">Правило авторизации создает ссылки в виде универсального кода ресурса (URI), основанных на различных уровнях разрешений.</span><span class="sxs-lookup"><span data-stu-id="f7c6a-109">An authorization rule will create links, as a URI, based on different permission levels.</span></span>
<span data-ttu-id="f7c6a-110">Клиенты направляются на один из этих URI на основе соответствующего уровня разрешений.</span><span class="sxs-lookup"><span data-stu-id="f7c6a-110">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="f7c6a-111">Например, клиент с разрешением на прослушивание будет направлен на универсальный код ресурса (URI) для этого разрешения.</span><span class="sxs-lookup"><span data-stu-id="f7c6a-111">For instance, a client with the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="f7c6a-112">Командлет **Get-AzNotificationHubAuthorizationRule** возвращает сведения только о правилах авторизации, связанных с центром уведомлений.</span><span class="sxs-lookup"><span data-stu-id="f7c6a-112">The **Get-AzNotificationHubAuthorizationRule** cmdlet only gets information about the authorization rules associated with a notification hub.</span></span>
<span data-ttu-id="f7c6a-113">Для получения сведений об основном центре используйте Get-AzNotificationHub.</span><span class="sxs-lookup"><span data-stu-id="f7c6a-113">To get information about the hub itself, use Get-AzNotificationHub.</span></span>

## <span data-ttu-id="f7c6a-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f7c6a-114">EXAMPLES</span></span>

### <span data-ttu-id="f7c6a-115">Пример 1: получение сведений обо всех правилах авторизации, назначенных для концентратора уведомлений</span><span class="sxs-lookup"><span data-stu-id="f7c6a-115">Example 1: Get information for all authorization rules assigned to a notification hub</span></span>
```
PS C:\>Get-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="f7c6a-116">Эта команда получает сведения обо всех правилах авторизации, назначенных концентратору уведомлений с именем ContosoInternalHub в пространстве имен ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="f7c6a-116">This command gets information for all the authorization rules assigned to the notification hub named ContosoInternalHub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="f7c6a-117">Необходимо указать пространство имен, в котором расположен Центральный центр, а также группу ресурсов, которой назначен концентратор.</span><span class="sxs-lookup"><span data-stu-id="f7c6a-117">You must specify the namespace where the hub is located as well as the resource group that the hub has been assigned to.</span></span>

### <span data-ttu-id="f7c6a-118">Пример 2: получение сведений о правилах авторизации, назначенных для концентратора уведомлений</span><span class="sxs-lookup"><span data-stu-id="f7c6a-118">Example 2: Get information for an authorization rules assigned to a notification hub</span></span>
```
PS C:\>Get-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="f7c6a-119">Эта команда получает сведения обо всех правилах авторизации, назначенных концентратору уведомлений с именем ContosoInternalHub в пространстве имен ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="f7c6a-119">This command gets information for all the authorization rules assigned to the notification hub named ContosoInternalHub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="f7c6a-120">В команде используется параметр *AuthorizationRule* , чтобы ограничить возвращаемые данные единственным правилом авторизации с именем ListenRule.</span><span class="sxs-lookup"><span data-stu-id="f7c6a-120">The command uses the *AuthorizationRule* parameter to limit the returned data to a single authorization rule named ListenRule.</span></span>

## <span data-ttu-id="f7c6a-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f7c6a-121">PARAMETERS</span></span>

### <span data-ttu-id="f7c6a-122">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f7c6a-122">-AuthorizationRule</span></span>
<span data-ttu-id="f7c6a-123">Указывает имя правила проверки подлинности SAS.</span><span class="sxs-lookup"><span data-stu-id="f7c6a-123">Specifies the name of an SAS authentication rule.</span></span>
<span data-ttu-id="f7c6a-124">Эти правила определяют тип доступа пользователей к концентратору уведомлений.</span><span class="sxs-lookup"><span data-stu-id="f7c6a-124">These rules determine the type of access that users have to the notification hub.</span></span>

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

### <span data-ttu-id="f7c6a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7c6a-125">-DefaultProfile</span></span>
<span data-ttu-id="f7c6a-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f7c6a-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f7c6a-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f7c6a-127">-Namespace</span></span>
<span data-ttu-id="f7c6a-128">Задает пространство имен, которому назначен Центр уведомлений.</span><span class="sxs-lookup"><span data-stu-id="f7c6a-128">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="f7c6a-129">Пространства имен обеспечивают способ группировки и классификации концентраторов уведомлений.</span><span class="sxs-lookup"><span data-stu-id="f7c6a-129">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="f7c6a-130">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="f7c6a-130">-NotificationHub</span></span>
<span data-ttu-id="f7c6a-131">Указывает центр уведомлений, которому этот командлет назначает правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="f7c6a-131">Specifies the notification hub that this cmdlet assigns authorization rules.</span></span>
<span data-ttu-id="f7c6a-132">Концентраторы уведомлений используются для отправки push-уведомлений нескольким клиентам вне зависимости от платформы, используемой этими клиентами.</span><span class="sxs-lookup"><span data-stu-id="f7c6a-132">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="f7c6a-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f7c6a-133">-ResourceGroup</span></span>
<span data-ttu-id="f7c6a-134">Указывает группу ресурсов, которой назначен Центр уведомлений.</span><span class="sxs-lookup"><span data-stu-id="f7c6a-134">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="f7c6a-135">Группы ресурсов организуют элементы, такие как пространства имен, концентраторы уведомлений и правила авторизации, в целях упрощения управления запасами и администрирования Azure.</span><span class="sxs-lookup"><span data-stu-id="f7c6a-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simplify inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="f7c6a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7c6a-136">CommonParameters</span></span>
<span data-ttu-id="f7c6a-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f7c6a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7c6a-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7c6a-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7c6a-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f7c6a-139">INPUTS</span></span>

### <span data-ttu-id="f7c6a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f7c6a-140">System.String</span></span>

## <span data-ttu-id="f7c6a-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7c6a-141">OUTPUTS</span></span>

### <span data-ttu-id="f7c6a-142">Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="f7c6a-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="f7c6a-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="f7c6a-143">NOTES</span></span>

## <span data-ttu-id="f7c6a-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f7c6a-144">RELATED LINKS</span></span>

[<span data-ttu-id="f7c6a-145">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f7c6a-145">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="f7c6a-146">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f7c6a-146">New-AzNotificationHubAuthorizationRule</span></span>](./New-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="f7c6a-147">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f7c6a-147">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="f7c6a-148">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f7c6a-148">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


