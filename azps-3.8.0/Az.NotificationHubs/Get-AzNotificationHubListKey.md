---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 326C87EB-EC3B-4B04-B593-EAC56FFA854A
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhublistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
ms.openlocfilehash: b8fdacf86de0e85c6f0ce241e743fc73066beb71
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065797"
---
# <span data-ttu-id="ec7dc-101">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="ec7dc-101">Get-AzNotificationHubListKey</span></span>

## <span data-ttu-id="ec7dc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ec7dc-102">SYNOPSIS</span></span>
<span data-ttu-id="ec7dc-103">Получает первичные и вторичные строки подключения, связанные с правилом авторизации концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="ec7dc-103">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

## <span data-ttu-id="ec7dc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ec7dc-104">SYNTAX</span></span>

```
Get-AzNotificationHubListKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec7dc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ec7dc-105">DESCRIPTION</span></span>
<span data-ttu-id="ec7dc-106">Командлет **Get-AzNotificationHubListKey** возвращает первичные и дополнительные строки подключения для правила авторизации на основе центра уведомлений (SA).</span><span class="sxs-lookup"><span data-stu-id="ec7dc-106">The **Get-AzNotificationHubListKey** cmdlet returns the primary and secondary connection strings of a notification hub Shared Access Signature (SAS) authorization rule.</span></span>
<span data-ttu-id="ec7dc-107">Правила авторизации управляют правами пользователей на разветвитель.</span><span class="sxs-lookup"><span data-stu-id="ec7dc-107">Authorization rules manage user rights to the hub.</span></span>
<span data-ttu-id="ec7dc-108">Каждое правило включает в себя первичную и вспомогательную строку подключения.</span><span class="sxs-lookup"><span data-stu-id="ec7dc-108">Each rule includes a primary and a secondary connection string.</span></span>
<span data-ttu-id="ec7dc-109">Эти строки подключения (URI) выполняют указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="ec7dc-109">These connection strings (URIs) perform the following:</span></span>
- <span data-ttu-id="ec7dc-110">Наведите пользователей на ресурс.</span><span class="sxs-lookup"><span data-stu-id="ec7dc-110">Point users to a resource.</span></span>
- <span data-ttu-id="ec7dc-111">Добавьте токен, содержащий параметры запроса.</span><span class="sxs-lookup"><span data-stu-id="ec7dc-111">Include a token containing query parameters.</span></span>
<span data-ttu-id="ec7dc-112">Один из этих параметров — подпись используется для проверки подлинности пользователя и предоставления указанного уровня доступа.</span><span class="sxs-lookup"><span data-stu-id="ec7dc-112">One of these parameters, the signature, is used to authenticate the user and provide the specified level of access.</span></span>

## <span data-ttu-id="ec7dc-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ec7dc-113">EXAMPLES</span></span>

### <span data-ttu-id="ec7dc-114">Пример 1: получение первичных и дополнительных строк подключения для правила авторизации</span><span class="sxs-lookup"><span data-stu-id="ec7dc-114">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubListKey -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="ec7dc-115">Эта команда получает первичные и дополнительные строки подключения для правила авторизации ListenRule, правило, назначенное для концентратора уведомлений ContosoInternalHub.</span><span class="sxs-lookup"><span data-stu-id="ec7dc-115">This command gets the primary and secondary connection strings for the authorization rule ListenRule, a rule assigned to the ContosoInternalHub notification hub.</span></span>
<span data-ttu-id="ec7dc-116">Команда должна включать пространство имен HUB и группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ec7dc-116">The command must include the hub namespace and resource group.</span></span>

## <span data-ttu-id="ec7dc-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ec7dc-117">PARAMETERS</span></span>

### <span data-ttu-id="ec7dc-118">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ec7dc-118">-AuthorizationRule</span></span>
<span data-ttu-id="ec7dc-119">Указывает имя правила проверки подлинности для подписи общего доступа (SAS).</span><span class="sxs-lookup"><span data-stu-id="ec7dc-119">Specifies the name of a Shared Access Signature (SAS) authentication rule.</span></span>
<span data-ttu-id="ec7dc-120">Эти правила определяют тип доступа пользователей к концентратору уведомлений.</span><span class="sxs-lookup"><span data-stu-id="ec7dc-120">These rules determine the type of access that users have to the notification hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec7dc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec7dc-121">-DefaultProfile</span></span>
<span data-ttu-id="ec7dc-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ec7dc-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ec7dc-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ec7dc-123">-Namespace</span></span>
<span data-ttu-id="ec7dc-124">Задает пространство имен, которому назначен Центр уведомлений.</span><span class="sxs-lookup"><span data-stu-id="ec7dc-124">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="ec7dc-125">Пространства имен обеспечивают способ группировки и классификации концентраторов уведомлений.</span><span class="sxs-lookup"><span data-stu-id="ec7dc-125">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="ec7dc-126">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="ec7dc-126">-NotificationHub</span></span>
<span data-ttu-id="ec7dc-127">Указывает центр уведомлений, которому назначается правило авторизации с помощью этого командлета.</span><span class="sxs-lookup"><span data-stu-id="ec7dc-127">Specifies the notification hub that this cmdlet assigns an authorization rule to.</span></span>
<span data-ttu-id="ec7dc-128">Концентраторы уведомлений используются для отправки push-уведомлений нескольким клиентам вне зависимости от платформы, используемой этими клиентами.</span><span class="sxs-lookup"><span data-stu-id="ec7dc-128">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="ec7dc-129">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ec7dc-129">-ResourceGroup</span></span>
<span data-ttu-id="ec7dc-130">Указывает группу ресурсов, которой назначен Центр уведомлений.</span><span class="sxs-lookup"><span data-stu-id="ec7dc-130">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="ec7dc-131">Группы ресурсов организуют элементы, такие как пространства имен, концентраторы уведомлений и правила авторизации, в целях простого управления запасами и администрирования Azure.</span><span class="sxs-lookup"><span data-stu-id="ec7dc-131">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="ec7dc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec7dc-132">CommonParameters</span></span>
<span data-ttu-id="ec7dc-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ec7dc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec7dc-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec7dc-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec7dc-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ec7dc-135">INPUTS</span></span>

### <span data-ttu-id="ec7dc-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ec7dc-136">System.String</span></span>

## <span data-ttu-id="ec7dc-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ec7dc-137">OUTPUTS</span></span>

### <span data-ttu-id="ec7dc-138">Microsoft. Azure. Management. NotificationHubs. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="ec7dc-138">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="ec7dc-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="ec7dc-139">NOTES</span></span>

## <span data-ttu-id="ec7dc-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ec7dc-140">RELATED LINKS</span></span>

[<span data-ttu-id="ec7dc-141">Get-AzNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="ec7dc-141">Get-AzNotificationHubAuthorizationRules</span></span>](./Get-AzNotificationHubAuthorizationRules.md)


