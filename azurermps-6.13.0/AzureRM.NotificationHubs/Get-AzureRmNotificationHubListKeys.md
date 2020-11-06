---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 326C87EB-EC3B-4B04-B593-EAC56FFA854A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhublistkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubListKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubListKeys.md
ms.openlocfilehash: 05c6ce89577e3c24368ddf47a0dec0abfeb2a388
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565824"
---
# <span data-ttu-id="7a72a-101">Get-AzureRmNotificationHubListKeys</span><span class="sxs-lookup"><span data-stu-id="7a72a-101">Get-AzureRmNotificationHubListKeys</span></span>

## <span data-ttu-id="7a72a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7a72a-102">SYNOPSIS</span></span>
<span data-ttu-id="7a72a-103">Получает первичные и вторичные строки подключения, связанные с правилом авторизации концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="7a72a-103">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a72a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7a72a-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubListKeys [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a72a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a72a-105">DESCRIPTION</span></span>
<span data-ttu-id="7a72a-106">Командлет **Get-AzureRmNotificationHubListKeys** возвращает первичные и дополнительные строки подключения для правила авторизации на основе центра уведомлений (SA).</span><span class="sxs-lookup"><span data-stu-id="7a72a-106">The **Get-AzureRmNotificationHubListKeys** cmdlet returns the primary and secondary connection strings of a notification hub Shared Access Signature (SAS) authorization rule.</span></span>
<span data-ttu-id="7a72a-107">Правила авторизации управляют правами пользователей на разветвитель.</span><span class="sxs-lookup"><span data-stu-id="7a72a-107">Authorization rules manage user rights to the hub.</span></span>
<span data-ttu-id="7a72a-108">Каждое правило включает в себя первичную и вспомогательную строку подключения.</span><span class="sxs-lookup"><span data-stu-id="7a72a-108">Each rule includes a primary and a secondary connection string.</span></span>
<span data-ttu-id="7a72a-109">Эти строки подключения (URI) выполняют указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="7a72a-109">These connection strings (URIs) perform the following:</span></span>
- <span data-ttu-id="7a72a-110">Наведите пользователей на ресурс.</span><span class="sxs-lookup"><span data-stu-id="7a72a-110">Point users to a resource.</span></span>
- <span data-ttu-id="7a72a-111">Добавьте токен, содержащий параметры запроса.</span><span class="sxs-lookup"><span data-stu-id="7a72a-111">Include a token containing query parameters.</span></span>
<span data-ttu-id="7a72a-112">Один из этих параметров — подпись используется для проверки подлинности пользователя и предоставления указанного уровня доступа.</span><span class="sxs-lookup"><span data-stu-id="7a72a-112">One of these parameters, the signature, is used to authenticate the user and provide the specified level of access.</span></span>

## <span data-ttu-id="7a72a-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7a72a-113">EXAMPLES</span></span>

### <span data-ttu-id="7a72a-114">Пример 1: получение первичных и дополнительных строк подключения для правила авторизации</span><span class="sxs-lookup"><span data-stu-id="7a72a-114">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzureRmNotificationHubListKeys -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="7a72a-115">Эта команда получает первичные и дополнительные строки подключения для правила авторизации ListenRule, правило, назначенное для концентратора уведомлений ContosoInternalHub.</span><span class="sxs-lookup"><span data-stu-id="7a72a-115">This command gets the primary and secondary connection strings for the authorization rule ListenRule, a rule assigned to the ContosoInternalHub notification hub.</span></span>
<span data-ttu-id="7a72a-116">Команда должна включать пространство имен HUB и группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7a72a-116">The command must include the hub namespace and resource group.</span></span>

## <span data-ttu-id="7a72a-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7a72a-117">PARAMETERS</span></span>

### <span data-ttu-id="7a72a-118">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7a72a-118">-AuthorizationRule</span></span>
<span data-ttu-id="7a72a-119">Указывает имя правила проверки подлинности для подписи общего доступа (SAS).</span><span class="sxs-lookup"><span data-stu-id="7a72a-119">Specifies the name of a Shared Access Signature (SAS) authentication rule.</span></span>
<span data-ttu-id="7a72a-120">Эти правила определяют тип доступа пользователей к концентратору уведомлений.</span><span class="sxs-lookup"><span data-stu-id="7a72a-120">These rules determine the type of access that users have to the notification hub.</span></span>

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

### <span data-ttu-id="7a72a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a72a-121">-DefaultProfile</span></span>
<span data-ttu-id="7a72a-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7a72a-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7a72a-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7a72a-123">-Namespace</span></span>
<span data-ttu-id="7a72a-124">Задает пространство имен, которому назначен Центр уведомлений.</span><span class="sxs-lookup"><span data-stu-id="7a72a-124">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="7a72a-125">Пространства имен обеспечивают способ группировки и классификации концентраторов уведомлений.</span><span class="sxs-lookup"><span data-stu-id="7a72a-125">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="7a72a-126">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="7a72a-126">-NotificationHub</span></span>
<span data-ttu-id="7a72a-127">Указывает центр уведомлений, которому назначается правило авторизации с помощью этого командлета.</span><span class="sxs-lookup"><span data-stu-id="7a72a-127">Specifies the notification hub that this cmdlet assigns an authorization rule to.</span></span>
<span data-ttu-id="7a72a-128">Концентраторы уведомлений используются для отправки push-уведомлений нескольким клиентам вне зависимости от платформы, используемой этими клиентами.</span><span class="sxs-lookup"><span data-stu-id="7a72a-128">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="7a72a-129">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7a72a-129">-ResourceGroup</span></span>
<span data-ttu-id="7a72a-130">Указывает группу ресурсов, которой назначен Центр уведомлений.</span><span class="sxs-lookup"><span data-stu-id="7a72a-130">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="7a72a-131">Группы ресурсов организуют элементы, такие как пространства имен, концентраторы уведомлений и правила авторизации, в целях простого управления запасами и администрирования Azure.</span><span class="sxs-lookup"><span data-stu-id="7a72a-131">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="7a72a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a72a-132">CommonParameters</span></span>
<span data-ttu-id="7a72a-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7a72a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a72a-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a72a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a72a-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7a72a-135">INPUTS</span></span>

### <span data-ttu-id="7a72a-136">System. String</span><span class="sxs-lookup"><span data-stu-id="7a72a-136">System.String</span></span>

## <span data-ttu-id="7a72a-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a72a-137">OUTPUTS</span></span>

### <span data-ttu-id="7a72a-138">Microsoft. Azure. Management. NotificationHubs. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="7a72a-138">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="7a72a-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="7a72a-139">NOTES</span></span>

## <span data-ttu-id="7a72a-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7a72a-140">RELATED LINKS</span></span>

[<span data-ttu-id="7a72a-141">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="7a72a-141">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)


