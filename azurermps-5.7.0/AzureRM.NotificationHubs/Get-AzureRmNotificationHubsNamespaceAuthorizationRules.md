---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhubsnamespaceauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: ade411d6d8ca19a5c17afd87388f9f7ab90d64d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569900"
---
# <span data-ttu-id="489bd-101">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="489bd-101">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>

## <span data-ttu-id="489bd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="489bd-102">SYNOPSIS</span></span>
<span data-ttu-id="489bd-103">Получает сведения о правилах авторизации, связанных с пространством имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="489bd-103">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="489bd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="489bd-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="489bd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="489bd-105">DESCRIPTION</span></span>
<span data-ttu-id="489bd-106">Командлет **Get-AzureRmNotificationHubsNamespaceAuthorizationRules** возвращает сведения о правилах авторизации для общих подписей доступа (SAS), связанных с пространством имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="489bd-106">The **Get-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet returns information about the Shared Access Signature (SAS) authorization rules associated with a notification hub namespace.</span></span>
<span data-ttu-id="489bd-107">Вы можете вернуть сведения обо всех правилах, связанных с пространством имен.</span><span class="sxs-lookup"><span data-stu-id="489bd-107">You can return information about all the rules associated with the namespace.</span></span>
<span data-ttu-id="489bd-108">Кроме того, с помощью параметра *AuthorizationRule* можно вернуть сведения о конкретном правиле.</span><span class="sxs-lookup"><span data-stu-id="489bd-108">Alternatively, and by including the *AuthorizationRule* parameter, you can return information for a specific rule.</span></span>

<span data-ttu-id="489bd-109">Правила авторизации управляют доступом к пространствам имен.</span><span class="sxs-lookup"><span data-stu-id="489bd-109">Authorization rules manage access to namespaces.</span></span>
<span data-ttu-id="489bd-110">Это делается с помощью создания ссылок в виде URI, основанных на различных уровнях разрешений.</span><span class="sxs-lookup"><span data-stu-id="489bd-110">This is done through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="489bd-111">Уровни платформы могут быть одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="489bd-111">Platform levels can be one of the following:</span></span> 

- <span data-ttu-id="489bd-112">Прослушивающих</span><span class="sxs-lookup"><span data-stu-id="489bd-112">Listen</span></span>
- <span data-ttu-id="489bd-113">Отправить</span><span class="sxs-lookup"><span data-stu-id="489bd-113">Send</span></span>
- <span data-ttu-id="489bd-114">Этими</span><span class="sxs-lookup"><span data-stu-id="489bd-114">Manage</span></span>

<span data-ttu-id="489bd-115">Клиенты направляются на один из этих URI на основе соответствующего уровня разрешений.</span><span class="sxs-lookup"><span data-stu-id="489bd-115">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="489bd-116">Например, клиент, которому предоставлено разрешение прослушивания, будет направлен на универсальный код ресурса (URI) для этого разрешения.</span><span class="sxs-lookup"><span data-stu-id="489bd-116">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>

<span data-ttu-id="489bd-117">Этот командлет получает только те правила авторизации, которые связаны с пространством имен.</span><span class="sxs-lookup"><span data-stu-id="489bd-117">This cmdlet only gets the authorization rules associated with a namespace.</span></span>
<span data-ttu-id="489bd-118">Чтобы получить сведения о пространстве имен, используйте Get-AzureRmNotificationHubsNamespace.</span><span class="sxs-lookup"><span data-stu-id="489bd-118">To get information about the namespace itself, use Get-AzureRmNotificationHubsNamespace.</span></span>

## <span data-ttu-id="489bd-119">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="489bd-119">EXAMPLES</span></span>

### <span data-ttu-id="489bd-120">Пример 1: получение сведений обо всех правилах авторизации, назначенных пространствам имен</span><span class="sxs-lookup"><span data-stu-id="489bd-120">Example 1: Get information about all authorization rules assigned to namespaces</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="489bd-121">Эта команда получает сведения обо всех правилах авторизации, назначенных для группы ресурсов Namespace ContosoNamespace и ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="489bd-121">This command gets information about all the authorization rules assigned to both the namespace ContosoNamespace and the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="489bd-122">Пример 2: получение сведений о правиле авторизации</span><span class="sxs-lookup"><span data-stu-id="489bd-122">Example 2: Get information about an authorization rule</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="489bd-123">Эта команда получает сведения о одном правиле авторизации пространства имен с именем ListenRule.</span><span class="sxs-lookup"><span data-stu-id="489bd-123">This command gets information about a single namespace authorization rule named ListenRule.</span></span>
<span data-ttu-id="489bd-124">При получении сведений о конкретном правиле авторизации необходимо включать пространство имен и группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="489bd-124">You must include the namespace and the resource group when you get information for a specific authorization rule.</span></span>

## <span data-ttu-id="489bd-125">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="489bd-125">PARAMETERS</span></span>

### <span data-ttu-id="489bd-126">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="489bd-126">-AuthorizationRule</span></span>
<span data-ttu-id="489bd-127">Указывает имя правила проверки подлинности SAS.</span><span class="sxs-lookup"><span data-stu-id="489bd-127">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="489bd-128">Эти правила определяют тип доступа пользователей к пространству имен.</span><span class="sxs-lookup"><span data-stu-id="489bd-128">These rules determine the type of access that users have to the namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="489bd-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="489bd-129">-DefaultProfile</span></span>
<span data-ttu-id="489bd-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="489bd-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="489bd-131">-Namespace</span><span class="sxs-lookup"><span data-stu-id="489bd-131">-Namespace</span></span>
<span data-ttu-id="489bd-132">Задает пространство имен, которым назначены правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="489bd-132">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="489bd-133">Пространства имен обеспечивают способ группировки и классификации концентраторов уведомлений.</span><span class="sxs-lookup"><span data-stu-id="489bd-133">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="489bd-134">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="489bd-134">-ResourceGroup</span></span>
<span data-ttu-id="489bd-135">Указывает группу ресурсов, которой назначены правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="489bd-135">Specifies the resource group to which the authorization rules are assigned.</span></span>

<span data-ttu-id="489bd-136">Группы ресурсов организуют элементы, такие как пространства имен, концентраторы уведомлений и правила авторизации, в целях простого управления запасами и администрирования Azure.</span><span class="sxs-lookup"><span data-stu-id="489bd-136">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="489bd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="489bd-137">CommonParameters</span></span>
<span data-ttu-id="489bd-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="489bd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="489bd-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="489bd-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="489bd-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="489bd-140">INPUTS</span></span>

### <span data-ttu-id="489bd-141">Ничего</span><span class="sxs-lookup"><span data-stu-id="489bd-141">None</span></span>
<span data-ttu-id="489bd-142">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="489bd-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="489bd-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="489bd-143">OUTPUTS</span></span>

### <span data-ttu-id="489bd-144">System. Collections. Generic. List ' 1 [Microsoft. Azure. SharedAccessAuthorizationRuleAttributes]</span><span class="sxs-lookup"><span data-stu-id="489bd-144">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes]</span></span>

## <span data-ttu-id="489bd-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="489bd-145">NOTES</span></span>

## <span data-ttu-id="489bd-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="489bd-146">RELATED LINKS</span></span>

[<span data-ttu-id="489bd-147">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="489bd-147">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="489bd-148">New-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="489bd-148">New-AzureRmNotificationHubsNamespace</span></span>](./New-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="489bd-149">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="489bd-149">Remove-AzureRmNotificationHubsNamespace</span></span>](./Remove-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="489bd-150">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="489bd-150">Set-AzureRmNotificationHubsNamespace</span></span>](./Set-AzureRmNotificationHubsNamespace.md)


