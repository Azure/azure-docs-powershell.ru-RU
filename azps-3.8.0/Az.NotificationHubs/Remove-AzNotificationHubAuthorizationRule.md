---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 715F8821-BBD1-440A-AD54-E960939E288A
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: d908d9d12e917efca6901c08bc69d4888072b6ef
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072775"
---
# <span data-ttu-id="bdc94-101">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bdc94-101">Remove-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="bdc94-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bdc94-102">SYNOPSIS</span></span>
<span data-ttu-id="bdc94-103">Удаляет правило авторизации из концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="bdc94-103">Removes an authorization rule from a notification hub.</span></span>

## <span data-ttu-id="bdc94-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bdc94-104">SYNTAX</span></span>

```
Remove-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdc94-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bdc94-105">DESCRIPTION</span></span>
<span data-ttu-id="bdc94-106">Командлет **Remove-AzNotificationHubAuthorizationRule** удаляет правило авторизации подписи общего доступа (SAS) из центра уведомлений.</span><span class="sxs-lookup"><span data-stu-id="bdc94-106">The **Remove-AzNotificationHubAuthorizationRule** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub.</span></span>
<span data-ttu-id="bdc94-107">Правила авторизации управляют доступом к концентраторам уведомлений с помощью создания ссылок, как URI, на основе различных уровней разрешений.</span><span class="sxs-lookup"><span data-stu-id="bdc94-107">Authorization rules manage access to your notification hubs through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="bdc94-108">Уровни разрешений могут быть одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="bdc94-108">Permission levels can be one of the following:</span></span> 
- <span data-ttu-id="bdc94-109">Прослушивающих</span><span class="sxs-lookup"><span data-stu-id="bdc94-109">Listen</span></span>
- <span data-ttu-id="bdc94-110">Отправить</span><span class="sxs-lookup"><span data-stu-id="bdc94-110">Send</span></span>
- <span data-ttu-id="bdc94-111">Управление клиентами направляется на один из этих URI на основе соответствующего уровня разрешений.</span><span class="sxs-lookup"><span data-stu-id="bdc94-111">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="bdc94-112">Например, клиент, которому предоставлено разрешение прослушивания, будет направлен на универсальный код ресурса (URI) для этого разрешения.</span><span class="sxs-lookup"><span data-stu-id="bdc94-112">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="bdc94-113">Удаление правила авторизации также приведет к удалению соответствующего разрешения пользователя.</span><span class="sxs-lookup"><span data-stu-id="bdc94-113">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="bdc94-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bdc94-114">EXAMPLES</span></span>

### <span data-ttu-id="bdc94-115">Пример 1: Удаление правила авторизации из центра уведомлений</span><span class="sxs-lookup"><span data-stu-id="bdc94-115">Example 1: Remove an authorization rule from a notification hub</span></span>
```
PS C:\>Remove-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -NotificationHub "ContosoExternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="bdc94-116">Эта команда удаляет правило авторизации с именем ListenRule из центра уведомлений с именем ContosoExternalHub.</span><span class="sxs-lookup"><span data-stu-id="bdc94-116">This command removes the authorization rule named ListenRule from the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="bdc94-117">При выполнении этой команды необходимо указать пространство имен и группу ресурсов, которым назначен концентратор.</span><span class="sxs-lookup"><span data-stu-id="bdc94-117">When you run this command you must specify both the namespace and the resource group that the hub is assigned to.</span></span>

## <span data-ttu-id="bdc94-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bdc94-118">PARAMETERS</span></span>

### <span data-ttu-id="bdc94-119">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bdc94-119">-AuthorizationRule</span></span>
<span data-ttu-id="bdc94-120">Указывает имя правила проверки подлинности SAS, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="bdc94-120">Specifies the name of the SAS authentication rule that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bdc94-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdc94-121">-DefaultProfile</span></span>
<span data-ttu-id="bdc94-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bdc94-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bdc94-123">-Force</span><span class="sxs-lookup"><span data-stu-id="bdc94-123">-Force</span></span>
<span data-ttu-id="bdc94-124">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="bdc94-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="bdc94-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="bdc94-125">-Namespace</span></span>
<span data-ttu-id="bdc94-126">Задает пространство имен, которому назначен Центр уведомлений.</span><span class="sxs-lookup"><span data-stu-id="bdc94-126">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="bdc94-127">Пространства имен обеспечивают способ группировки и классификации концентраторов уведомлений.</span><span class="sxs-lookup"><span data-stu-id="bdc94-127">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="bdc94-128">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="bdc94-128">-NotificationHub</span></span>
<span data-ttu-id="bdc94-129">Задает центр уведомлений, которому назначены правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="bdc94-129">Specifies the notification hub the authorization rules are assigned to.</span></span>
<span data-ttu-id="bdc94-130">Концентраторы уведомлений используются для отправки push-уведомлений нескольким клиентам вне зависимости от платформы.</span><span class="sxs-lookup"><span data-stu-id="bdc94-130">Notification hubs are used to send push notifications to multiple clients regardless of the platform.</span></span>

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

### <span data-ttu-id="bdc94-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bdc94-131">-ResourceGroup</span></span>
<span data-ttu-id="bdc94-132">Указывает группу ресурсов, которой назначен Центр уведомлений.</span><span class="sxs-lookup"><span data-stu-id="bdc94-132">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="bdc94-133">Группы ресурсов организуют элементы, такие как пространства имен, концентраторы уведомлений и правила авторизации, в целях простого управления запасами и администрирования Azure.</span><span class="sxs-lookup"><span data-stu-id="bdc94-133">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="bdc94-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bdc94-134">-Confirm</span></span>
<span data-ttu-id="bdc94-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bdc94-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdc94-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdc94-136">-WhatIf</span></span>
<span data-ttu-id="bdc94-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bdc94-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bdc94-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bdc94-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdc94-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdc94-139">CommonParameters</span></span>
<span data-ttu-id="bdc94-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bdc94-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdc94-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdc94-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdc94-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bdc94-142">INPUTS</span></span>

### <span data-ttu-id="bdc94-143">System. String</span><span class="sxs-lookup"><span data-stu-id="bdc94-143">System.String</span></span>

## <span data-ttu-id="bdc94-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bdc94-144">OUTPUTS</span></span>

### <span data-ttu-id="bdc94-145">System. void</span><span class="sxs-lookup"><span data-stu-id="bdc94-145">System.Void</span></span>

## <span data-ttu-id="bdc94-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="bdc94-146">NOTES</span></span>

## <span data-ttu-id="bdc94-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bdc94-147">RELATED LINKS</span></span>

[<span data-ttu-id="bdc94-148">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bdc94-148">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="bdc94-149">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bdc94-149">New-AzNotificationHubAuthorizationRule</span></span>](./New-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="bdc94-150">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bdc94-150">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


