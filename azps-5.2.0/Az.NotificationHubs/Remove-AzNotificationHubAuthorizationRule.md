---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 715F8821-BBD1-440A-AD54-E960939E288A
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: d908d9d12e917efca6901c08bc69d4888072b6ef
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395247"
---
# <span data-ttu-id="1d245-101">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1d245-101">Remove-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="1d245-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d245-102">SYNOPSIS</span></span>
<span data-ttu-id="1d245-103">Удаляет правило авторизации из концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="1d245-103">Removes an authorization rule from a notification hub.</span></span>

## <span data-ttu-id="1d245-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1d245-104">SYNTAX</span></span>

```
Remove-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d245-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1d245-105">DESCRIPTION</span></span>
<span data-ttu-id="1d245-106">Для удаления правила авторизации SAS из концентратора уведомлений удаляется правило авторизации **Remove-AzNotificationHubAuthorizationRule.**</span><span class="sxs-lookup"><span data-stu-id="1d245-106">The **Remove-AzNotificationHubAuthorizationRule** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub.</span></span>
<span data-ttu-id="1d245-107">Правила авторизации управляют доступом к концентраторам уведомлений путем создания ссылок в качестве ЮРИС на основе различных уровней разрешений.</span><span class="sxs-lookup"><span data-stu-id="1d245-107">Authorization rules manage access to your notification hubs through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="1d245-108">Уровни разрешений могут быть следующими:</span><span class="sxs-lookup"><span data-stu-id="1d245-108">Permission levels can be one of the following:</span></span> 
- <span data-ttu-id="1d245-109">Прослушивание</span><span class="sxs-lookup"><span data-stu-id="1d245-109">Listen</span></span>
- <span data-ttu-id="1d245-110">Отправить</span><span class="sxs-lookup"><span data-stu-id="1d245-110">Send</span></span>
- <span data-ttu-id="1d245-111">Управление клиентами направляется на один из этих URL-адресов с учетом соответствующего уровня разрешений.</span><span class="sxs-lookup"><span data-stu-id="1d245-111">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="1d245-112">Например, клиент с разрешением на прослушивание будет направлен в URI для этого разрешения.</span><span class="sxs-lookup"><span data-stu-id="1d245-112">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="1d245-113">При удалении правила авторизации также удаляется соответствующее разрешение пользователя.</span><span class="sxs-lookup"><span data-stu-id="1d245-113">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="1d245-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1d245-114">EXAMPLES</span></span>

### <span data-ttu-id="1d245-115">Пример 1. Удаление правила авторизации из концентратора уведомлений</span><span class="sxs-lookup"><span data-stu-id="1d245-115">Example 1: Remove an authorization rule from a notification hub</span></span>
```
PS C:\>Remove-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -NotificationHub "ContosoExternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="1d245-116">Эта команда удаляет правило авторизации listenRule из концентратора уведомлений ContosoExternalHub.</span><span class="sxs-lookup"><span data-stu-id="1d245-116">This command removes the authorization rule named ListenRule from the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="1d245-117">При запуске этой команды необходимо указать пространство имен и группу ресурсов, назначенную центру.</span><span class="sxs-lookup"><span data-stu-id="1d245-117">When you run this command you must specify both the namespace and the resource group that the hub is assigned to.</span></span>

## <span data-ttu-id="1d245-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d245-118">PARAMETERS</span></span>

### <span data-ttu-id="1d245-119">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1d245-119">-AuthorizationRule</span></span>
<span data-ttu-id="1d245-120">Указывает имя правила проверки подлинности SAS, которое удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d245-120">Specifies the name of the SAS authentication rule that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1d245-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d245-121">-DefaultProfile</span></span>
<span data-ttu-id="1d245-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1d245-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1d245-123">-Force</span><span class="sxs-lookup"><span data-stu-id="1d245-123">-Force</span></span>
<span data-ttu-id="1d245-124">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="1d245-124">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d245-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1d245-125">-Namespace</span></span>
<span data-ttu-id="1d245-126">Определяет пространство имен, которому назначен концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="1d245-126">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="1d245-127">Пространства имен предоставляют возможность группировать и классифицировать концентраторы уведомлений.</span><span class="sxs-lookup"><span data-stu-id="1d245-127">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="1d245-128">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="1d245-128">-NotificationHub</span></span>
<span data-ttu-id="1d245-129">Указывает центр уведомлений, который назначен правилам авторизации.</span><span class="sxs-lookup"><span data-stu-id="1d245-129">Specifies the notification hub the authorization rules are assigned to.</span></span>
<span data-ttu-id="1d245-130">Концентраторы уведомлений используются для отправки push-уведомлений нескольким клиентам независимо от платформы.</span><span class="sxs-lookup"><span data-stu-id="1d245-130">Notification hubs are used to send push notifications to multiple clients regardless of the platform.</span></span>

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

### <span data-ttu-id="1d245-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1d245-131">-ResourceGroup</span></span>
<span data-ttu-id="1d245-132">Группа ресурсов, которой назначен концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="1d245-132">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="1d245-133">Группы ресурсов упорядочиют такие элементы, как пространства имен, концентраторы уведомлений и правила авторизации, чтобы упрость управление запасами и администрирование Azure.</span><span class="sxs-lookup"><span data-stu-id="1d245-133">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="1d245-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1d245-134">-Confirm</span></span>
<span data-ttu-id="1d245-135">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="1d245-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d245-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d245-136">-WhatIf</span></span>
<span data-ttu-id="1d245-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d245-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1d245-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1d245-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d245-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d245-139">CommonParameters</span></span>
<span data-ttu-id="1d245-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d245-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d245-141">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d245-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d245-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1d245-142">INPUTS</span></span>

### <span data-ttu-id="1d245-143">System.String</span><span class="sxs-lookup"><span data-stu-id="1d245-143">System.String</span></span>

## <span data-ttu-id="1d245-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1d245-144">OUTPUTS</span></span>

### <span data-ttu-id="1d245-145">System.Void</span><span class="sxs-lookup"><span data-stu-id="1d245-145">System.Void</span></span>

## <span data-ttu-id="1d245-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1d245-146">NOTES</span></span>

## <span data-ttu-id="1d245-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1d245-147">RELATED LINKS</span></span>

[<span data-ttu-id="1d245-148">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1d245-148">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="1d245-149">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1d245-149">New-AzNotificationHubAuthorizationRule</span></span>](./New-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="1d245-150">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1d245-150">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


