---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 7A9D8F5A-6035-411B-8FDB-96ABFEED05A2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: 5d2398e86a5507e5672dba46cafbbb1f27c402a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569280"
---
# <span data-ttu-id="29b69-101">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="29b69-101">Get-AzureRmNotificationHubAuthorizationRules</span></span>

## <span data-ttu-id="29b69-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="29b69-102">SYNOPSIS</span></span>
<span data-ttu-id="29b69-103">Получает сведения о правилах авторизации, связанных с центром уведомлений.</span><span class="sxs-lookup"><span data-stu-id="29b69-103">Gets information about the authorization rules associated with a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29b69-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="29b69-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="29b69-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="29b69-105">DESCRIPTION</span></span>
<span data-ttu-id="29b69-106">Командлет **Get-AzureRmNotificationHubAuthorizationRules** получает сведения о правилах авторизации для общих подписей доступа (SAS), связанных с центром уведомлений.</span><span class="sxs-lookup"><span data-stu-id="29b69-106">The **Get-AzureRmNotificationHubAuthorizationRules** cmdlet gets information about the Shared Access Signature (SAS) authorization rules associated with a notification hub.</span></span>
<span data-ttu-id="29b69-107">Командлет возвращает сведения о конкретном правиле, а также о всех правилах, связанных с основным приложением или с помощью параметра *AuthorizationRule* .</span><span class="sxs-lookup"><span data-stu-id="29b69-107">The cmdlet returns information about all the rules associated with a hub or, by including the *AuthorizationRule* parameter, gets information about a specific rule.</span></span>

<span data-ttu-id="29b69-108">Правила авторизации управляют доступом к концентраторам уведомлений.</span><span class="sxs-lookup"><span data-stu-id="29b69-108">Authorization rules manage access to your notification hubs.</span></span>
<span data-ttu-id="29b69-109">Правило авторизации создает ссылки в виде универсального кода ресурса (URI), основанных на различных уровнях разрешений.</span><span class="sxs-lookup"><span data-stu-id="29b69-109">An authorization rule will create links, as a URI, based on different permission levels.</span></span>
<span data-ttu-id="29b69-110">Клиенты направляются на один из этих URI на основе соответствующего уровня разрешений.</span><span class="sxs-lookup"><span data-stu-id="29b69-110">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="29b69-111">Например, клиент с разрешением на прослушивание будет направлен на универсальный код ресурса (URI) для этого разрешения.</span><span class="sxs-lookup"><span data-stu-id="29b69-111">For instance, a client with the Listen permission will be directed to the URI for that permission.</span></span>

<span data-ttu-id="29b69-112">Командлет **Get-AzureRmNotificationHubAuthorizationRules** возвращает сведения только о правилах авторизации, связанных с центром уведомлений.</span><span class="sxs-lookup"><span data-stu-id="29b69-112">The **Get-AzureRmNotificationHubAuthorizationRules** cmdlet only gets information about the authorization rules associated with a notification hub.</span></span>
<span data-ttu-id="29b69-113">Для получения сведений об основном центре используйте Get-AzureRmNotificationHub.</span><span class="sxs-lookup"><span data-stu-id="29b69-113">To get information about the hub itself, use Get-AzureRmNotificationHub.</span></span>

## <span data-ttu-id="29b69-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="29b69-114">EXAMPLES</span></span>

### <span data-ttu-id="29b69-115">Пример 1: получение сведений обо всех правилах авторизации, назначенных для концентратора уведомлений</span><span class="sxs-lookup"><span data-stu-id="29b69-115">Example 1: Get information for all authorization rules assigned to a notification hub</span></span>
```
PS C:\>Get-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="29b69-116">Эта команда получает сведения обо всех правилах авторизации, назначенных концентратору уведомлений с именем ContosoInternalHub в пространстве имен ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="29b69-116">This command gets information for all the authorization rules assigned to the notification hub named ContosoInternalHub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="29b69-117">Необходимо указать пространство имен, в котором расположен Центральный центр, а также группу ресурсов, которой назначен концентратор.</span><span class="sxs-lookup"><span data-stu-id="29b69-117">You must specify the namespace where the hub is located as well as the resource group that the hub has been assigned to.</span></span>

### <span data-ttu-id="29b69-118">Пример 2: получение сведений о правилах авторизации, назначенных для концентратора уведомлений</span><span class="sxs-lookup"><span data-stu-id="29b69-118">Example 2: Get information for an authorization rules assigned to a notification hub</span></span>
```
PS C:\>Get-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="29b69-119">Эта команда получает сведения обо всех правилах авторизации, назначенных концентратору уведомлений с именем ContosoInternalHub в пространстве имен ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="29b69-119">This command gets information for all the authorization rules assigned to the notification hub named ContosoInternalHub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="29b69-120">В команде используется параметр *AuthorizationRule* , чтобы ограничить возвращаемые данные единственным правилом авторизации с именем ListenRule.</span><span class="sxs-lookup"><span data-stu-id="29b69-120">The command uses the *AuthorizationRule* parameter to limit the returned data to a single authorization rule named ListenRule.</span></span>

## <span data-ttu-id="29b69-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="29b69-121">PARAMETERS</span></span>

### <span data-ttu-id="29b69-122">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="29b69-122">-AuthorizationRule</span></span>
<span data-ttu-id="29b69-123">Указывает имя правила проверки подлинности SAS.</span><span class="sxs-lookup"><span data-stu-id="29b69-123">Specifies the name of an SAS authentication rule.</span></span>
<span data-ttu-id="29b69-124">Эти правила определяют тип доступа пользователей к концентратору уведомлений.</span><span class="sxs-lookup"><span data-stu-id="29b69-124">These rules determine the type of access that users have to the notification hub.</span></span>

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

### <span data-ttu-id="29b69-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="29b69-125">-Namespace</span></span>
<span data-ttu-id="29b69-126">Задает пространство имен, которому назначен Центр уведомлений.</span><span class="sxs-lookup"><span data-stu-id="29b69-126">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="29b69-127">Пространства имен обеспечивают способ группировки и классификации концентраторов уведомлений.</span><span class="sxs-lookup"><span data-stu-id="29b69-127">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="29b69-128">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="29b69-128">-NotificationHub</span></span>
<span data-ttu-id="29b69-129">Указывает центр уведомлений, которому этот командлет назначает правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="29b69-129">Specifies the notification hub that this cmdlet assigns authorization rules.</span></span>
<span data-ttu-id="29b69-130">Концентраторы уведомлений используются для отправки push-уведомлений нескольким клиентам вне зависимости от платформы, используемой этими клиентами.</span><span class="sxs-lookup"><span data-stu-id="29b69-130">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="29b69-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="29b69-131">-ResourceGroup</span></span>
<span data-ttu-id="29b69-132">Указывает группу ресурсов, которой назначен Центр уведомлений.</span><span class="sxs-lookup"><span data-stu-id="29b69-132">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="29b69-133">Группы ресурсов организуют элементы, такие как пространства имен, концентраторы уведомлений и правила авторизации, в целях упрощения управления запасами и администрирования Azure.</span><span class="sxs-lookup"><span data-stu-id="29b69-133">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simplify inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="29b69-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29b69-134">-DefaultProfile</span></span>
<span data-ttu-id="29b69-135">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="29b69-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29b69-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29b69-136">CommonParameters</span></span>
<span data-ttu-id="29b69-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="29b69-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29b69-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29b69-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29b69-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="29b69-139">INPUTS</span></span>

## <span data-ttu-id="29b69-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="29b69-140">OUTPUTS</span></span>

### <span data-ttu-id="29b69-141">System. Collections. Generic. List ' 1 [Microsoft. Azure. SharedAccessAuthorizationRuleAttributes]</span><span class="sxs-lookup"><span data-stu-id="29b69-141">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes]</span></span>

## <span data-ttu-id="29b69-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="29b69-142">NOTES</span></span>

## <span data-ttu-id="29b69-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="29b69-143">RELATED LINKS</span></span>

[<span data-ttu-id="29b69-144">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="29b69-144">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="29b69-145">New-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="29b69-145">New-AzureRmNotificationHubAuthorizationRules</span></span>](./New-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="29b69-146">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="29b69-146">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="29b69-147">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="29b69-147">Set-AzureRmNotificationHubAuthorizationRules</span></span>](./Set-AzureRmNotificationHubAuthorizationRules.md)


