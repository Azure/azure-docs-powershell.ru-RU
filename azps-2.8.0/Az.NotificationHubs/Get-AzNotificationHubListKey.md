---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 326C87EB-EC3B-4B04-B593-EAC56FFA854A
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhublistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
ms.openlocfilehash: 7ce6c3c08c1794e2bed794186203a5c6c0d1fdea
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100413767"
---
# <span data-ttu-id="fe1dc-101">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="fe1dc-101">Get-AzNotificationHubListKey</span></span>

## <span data-ttu-id="fe1dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe1dc-102">SYNOPSIS</span></span>
<span data-ttu-id="fe1dc-103">Возвращает основные и дополнительные строки подключения, связанные с правилом авторизации концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="fe1dc-103">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

## <span data-ttu-id="fe1dc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fe1dc-104">SYNTAX</span></span>

```
Get-AzNotificationHubListKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe1dc-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe1dc-105">DESCRIPTION</span></span>
<span data-ttu-id="fe1dc-106">Чтобы **получить основное** и дополнительное строки подключения для правила авторизации SAS, можно получить главное и дополнительное строки подключения для правила авторизации в Центре уведомлений Shared Access Signature (SAS).</span><span class="sxs-lookup"><span data-stu-id="fe1dc-106">The **Get-AzNotificationHubListKey** cmdlet returns the primary and secondary connection strings of a notification hub Shared Access Signature (SAS) authorization rule.</span></span>
<span data-ttu-id="fe1dc-107">Правила авторизации управляют правами пользователей на центр.</span><span class="sxs-lookup"><span data-stu-id="fe1dc-107">Authorization rules manage user rights to the hub.</span></span>
<span data-ttu-id="fe1dc-108">Каждое правило содержит основную и вторичную строку подключения.</span><span class="sxs-lookup"><span data-stu-id="fe1dc-108">Each rule includes a primary and a secondary connection string.</span></span>
<span data-ttu-id="fe1dc-109">Эти строки подключения ( URIS) выполняют указанные ниже точки.</span><span class="sxs-lookup"><span data-stu-id="fe1dc-109">These connection strings (URIs) perform the following:</span></span>
- <span data-ttu-id="fe1dc-110">Наказать пользователей на ресурс.</span><span class="sxs-lookup"><span data-stu-id="fe1dc-110">Point users to a resource.</span></span>
- <span data-ttu-id="fe1dc-111">Включайте маркер, содержащий параметры запроса.</span><span class="sxs-lookup"><span data-stu-id="fe1dc-111">Include a token containing query parameters.</span></span>
<span data-ttu-id="fe1dc-112">Один из этих параметров ( подпись) используется для проверки подлинности пользователя и предоставления указанного уровня доступа.</span><span class="sxs-lookup"><span data-stu-id="fe1dc-112">One of these parameters, the signature, is used to authenticate the user and provide the specified level of access.</span></span>

## <span data-ttu-id="fe1dc-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fe1dc-113">EXAMPLES</span></span>

### <span data-ttu-id="fe1dc-114">Пример 1. Получите основные и дополнительные строки подключения для правила авторизации</span><span class="sxs-lookup"><span data-stu-id="fe1dc-114">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubListKey -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="fe1dc-115">Эта команда получает основные и дополнительные строки подключения для правила авторизации ListenRule — правила, назначенного концентратору уведомлений ContosoInternalHub.</span><span class="sxs-lookup"><span data-stu-id="fe1dc-115">This command gets the primary and secondary connection strings for the authorization rule ListenRule, a rule assigned to the ContosoInternalHub notification hub.</span></span>
<span data-ttu-id="fe1dc-116">Команда должна включать пространство имен концентратора и группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fe1dc-116">The command must include the hub namespace and resource group.</span></span>

## <span data-ttu-id="fe1dc-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe1dc-117">PARAMETERS</span></span>

### <span data-ttu-id="fe1dc-118">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="fe1dc-118">-AuthorizationRule</span></span>
<span data-ttu-id="fe1dc-119">Указывает имя правила проверки подлинности SAS.</span><span class="sxs-lookup"><span data-stu-id="fe1dc-119">Specifies the name of a Shared Access Signature (SAS) authentication rule.</span></span>
<span data-ttu-id="fe1dc-120">Эти правила определяют тип доступа пользователей к центру уведомлений.</span><span class="sxs-lookup"><span data-stu-id="fe1dc-120">These rules determine the type of access that users have to the notification hub.</span></span>

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

### <span data-ttu-id="fe1dc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe1dc-121">-DefaultProfile</span></span>
<span data-ttu-id="fe1dc-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="fe1dc-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe1dc-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="fe1dc-123">-Namespace</span></span>
<span data-ttu-id="fe1dc-124">Определяет пространство имен, которому назначен концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="fe1dc-124">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="fe1dc-125">Пространства имен предоставляют возможность группировать концентраторы уведомлений и классифицировать их.</span><span class="sxs-lookup"><span data-stu-id="fe1dc-125">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="fe1dc-126">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="fe1dc-126">-NotificationHub</span></span>
<span data-ttu-id="fe1dc-127">Указывает центр уведомлений, для который этот cmdlet назначает правило авторизации.</span><span class="sxs-lookup"><span data-stu-id="fe1dc-127">Specifies the notification hub that this cmdlet assigns an authorization rule to.</span></span>
<span data-ttu-id="fe1dc-128">Концентраторы уведомлений используются для отправки push-уведомлений нескольким клиентам независимо от платформы, используемой этими клиентами.</span><span class="sxs-lookup"><span data-stu-id="fe1dc-128">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="fe1dc-129">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fe1dc-129">-ResourceGroup</span></span>
<span data-ttu-id="fe1dc-130">Группа ресурсов, которой назначен концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="fe1dc-130">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="fe1dc-131">Группы ресурсов упорядочиют такие элементы, как пространства имен, концентраторы уведомлений и правила авторизации, чтобы упрость управление запасами и администрирование Azure.</span><span class="sxs-lookup"><span data-stu-id="fe1dc-131">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="fe1dc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe1dc-132">CommonParameters</span></span>
<span data-ttu-id="fe1dc-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe1dc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe1dc-134">Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe1dc-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe1dc-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fe1dc-135">INPUTS</span></span>

### <span data-ttu-id="fe1dc-136">System.String</span><span class="sxs-lookup"><span data-stu-id="fe1dc-136">System.String</span></span>

## <span data-ttu-id="fe1dc-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fe1dc-137">OUTPUTS</span></span>

### <span data-ttu-id="fe1dc-138">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="fe1dc-138">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="fe1dc-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fe1dc-139">NOTES</span></span>

## <span data-ttu-id="fe1dc-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fe1dc-140">RELATED LINKS</span></span>



