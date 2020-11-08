---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: f3ba8428a6f6a9e618872e1292234751979b3c4b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244757"
---
# <span data-ttu-id="6568d-101">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6568d-101">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="6568d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6568d-102">SYNOPSIS</span></span>
<span data-ttu-id="6568d-103">Получает сведения о правилах авторизации, связанных с пространством имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="6568d-103">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

## <span data-ttu-id="6568d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6568d-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6568d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6568d-105">DESCRIPTION</span></span>
<span data-ttu-id="6568d-106">Командлет **Get-AzNotificationHubsNamespaceAuthorizationRule** возвращает сведения о правилах авторизации для общих подписей доступа (SAS), связанных с пространством имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="6568d-106">The **Get-AzNotificationHubsNamespaceAuthorizationRule** cmdlet returns information about the Shared Access Signature (SAS) authorization rules associated with a notification hub namespace.</span></span>
<span data-ttu-id="6568d-107">Вы можете вернуть сведения обо всех правилах, связанных с пространством имен.</span><span class="sxs-lookup"><span data-stu-id="6568d-107">You can return information about all the rules associated with the namespace.</span></span>
<span data-ttu-id="6568d-108">Кроме того, с помощью параметра *AuthorizationRule* можно вернуть сведения о конкретном правиле.</span><span class="sxs-lookup"><span data-stu-id="6568d-108">Alternatively, and by including the *AuthorizationRule* parameter, you can return information for a specific rule.</span></span>
<span data-ttu-id="6568d-109">Правила авторизации управляют доступом к пространствам имен.</span><span class="sxs-lookup"><span data-stu-id="6568d-109">Authorization rules manage access to namespaces.</span></span>
<span data-ttu-id="6568d-110">Это делается с помощью создания ссылок в виде URI, основанных на различных уровнях разрешений.</span><span class="sxs-lookup"><span data-stu-id="6568d-110">This is done through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="6568d-111">Уровни платформы могут быть одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="6568d-111">Platform levels can be one of the following:</span></span> 
- <span data-ttu-id="6568d-112">Прослушивающих</span><span class="sxs-lookup"><span data-stu-id="6568d-112">Listen</span></span>
- <span data-ttu-id="6568d-113">Отправить</span><span class="sxs-lookup"><span data-stu-id="6568d-113">Send</span></span>
- <span data-ttu-id="6568d-114">Управление клиентами направляется на один из этих URI на основе соответствующего уровня разрешений.</span><span class="sxs-lookup"><span data-stu-id="6568d-114">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="6568d-115">Например, клиент, которому предоставлено разрешение прослушивания, будет направлен на универсальный код ресурса (URI) для этого разрешения.</span><span class="sxs-lookup"><span data-stu-id="6568d-115">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="6568d-116">Этот командлет получает только те правила авторизации, которые связаны с пространством имен.</span><span class="sxs-lookup"><span data-stu-id="6568d-116">This cmdlet only gets the authorization rules associated with a namespace.</span></span>
<span data-ttu-id="6568d-117">Чтобы получить сведения о пространстве имен, используйте Get-AzNotificationHubsNamespace.</span><span class="sxs-lookup"><span data-stu-id="6568d-117">To get information about the namespace itself, use Get-AzNotificationHubsNamespace.</span></span>

## <span data-ttu-id="6568d-118">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6568d-118">EXAMPLES</span></span>

### <span data-ttu-id="6568d-119">Пример 1: получение сведений обо всех правилах авторизации, назначенных пространствам имен</span><span class="sxs-lookup"><span data-stu-id="6568d-119">Example 1: Get information about all authorization rules assigned to namespaces</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="6568d-120">Эта команда получает сведения обо всех правилах авторизации, назначенных для группы ресурсов Namespace ContosoNamespace и ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="6568d-120">This command gets information about all the authorization rules assigned to both the namespace ContosoNamespace and the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="6568d-121">Пример 2: получение сведений о правиле авторизации</span><span class="sxs-lookup"><span data-stu-id="6568d-121">Example 2: Get information about an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="6568d-122">Эта команда получает сведения о одном правиле авторизации пространства имен с именем ListenRule.</span><span class="sxs-lookup"><span data-stu-id="6568d-122">This command gets information about a single namespace authorization rule named ListenRule.</span></span>
<span data-ttu-id="6568d-123">При получении сведений о конкретном правиле авторизации необходимо включать пространство имен и группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6568d-123">You must include the namespace and the resource group when you get information for a specific authorization rule.</span></span>

## <span data-ttu-id="6568d-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6568d-124">PARAMETERS</span></span>

### <span data-ttu-id="6568d-125">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6568d-125">-AuthorizationRule</span></span>
<span data-ttu-id="6568d-126">Указывает имя правила проверки подлинности SAS.</span><span class="sxs-lookup"><span data-stu-id="6568d-126">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="6568d-127">Эти правила определяют тип доступа пользователей к пространству имен.</span><span class="sxs-lookup"><span data-stu-id="6568d-127">These rules determine the type of access that users have to the namespace.</span></span>

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

### <span data-ttu-id="6568d-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6568d-128">-DefaultProfile</span></span>
<span data-ttu-id="6568d-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6568d-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6568d-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6568d-130">-Namespace</span></span>
<span data-ttu-id="6568d-131">Задает пространство имен, которым назначены правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="6568d-131">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="6568d-132">Пространства имен обеспечивают способ группировки и классификации концентраторов уведомлений.</span><span class="sxs-lookup"><span data-stu-id="6568d-132">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="6568d-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6568d-133">-ResourceGroup</span></span>
<span data-ttu-id="6568d-134">Указывает группу ресурсов, которой назначены правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="6568d-134">Specifies the resource group to which the authorization rules are assigned.</span></span>
<span data-ttu-id="6568d-135">Группы ресурсов организуют элементы, такие как пространства имен, концентраторы уведомлений и правила авторизации, в целях простого управления запасами и администрирования Azure.</span><span class="sxs-lookup"><span data-stu-id="6568d-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="6568d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6568d-136">CommonParameters</span></span>
<span data-ttu-id="6568d-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6568d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6568d-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6568d-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6568d-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6568d-139">INPUTS</span></span>

### <span data-ttu-id="6568d-140">System. String</span><span class="sxs-lookup"><span data-stu-id="6568d-140">System.String</span></span>

## <span data-ttu-id="6568d-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6568d-141">OUTPUTS</span></span>

### <span data-ttu-id="6568d-142">Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="6568d-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="6568d-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="6568d-143">NOTES</span></span>

## <span data-ttu-id="6568d-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6568d-144">RELATED LINKS</span></span>

[<span data-ttu-id="6568d-145">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="6568d-145">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="6568d-146">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="6568d-146">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="6568d-147">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="6568d-147">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)

[<span data-ttu-id="6568d-148">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="6568d-148">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


