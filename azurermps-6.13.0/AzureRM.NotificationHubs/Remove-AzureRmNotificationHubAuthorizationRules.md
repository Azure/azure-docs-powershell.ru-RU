---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 715F8821-BBD1-440A-AD54-E960939E288A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/remove-azurermnotificationhubauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: 7e731052219c796b6e8453c64accd0cf8c25895a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564175"
---
# <span data-ttu-id="1bde7-101">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="1bde7-101">Remove-AzureRmNotificationHubAuthorizationRules</span></span>

## <span data-ttu-id="1bde7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1bde7-102">SYNOPSIS</span></span>
<span data-ttu-id="1bde7-103">Удаляет правило авторизации из концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="1bde7-103">Removes an authorization rule from a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1bde7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1bde7-104">SYNTAX</span></span>

```
Remove-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bde7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1bde7-105">DESCRIPTION</span></span>
<span data-ttu-id="1bde7-106">Командлет **Remove-AzureRmNotificationHubAuthorizationRules** удаляет правило авторизации подписи общего доступа (SAS) из центра уведомлений.</span><span class="sxs-lookup"><span data-stu-id="1bde7-106">The **Remove-AzureRmNotificationHubAuthorizationRules** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub.</span></span>
<span data-ttu-id="1bde7-107">Правила авторизации управляют доступом к концентраторам уведомлений с помощью создания ссылок, как URI, на основе различных уровней разрешений.</span><span class="sxs-lookup"><span data-stu-id="1bde7-107">Authorization rules manage access to your notification hubs through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="1bde7-108">Уровни разрешений могут быть одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="1bde7-108">Permission levels can be one of the following:</span></span> 
- <span data-ttu-id="1bde7-109">Прослушивающих</span><span class="sxs-lookup"><span data-stu-id="1bde7-109">Listen</span></span>
- <span data-ttu-id="1bde7-110">Отправить</span><span class="sxs-lookup"><span data-stu-id="1bde7-110">Send</span></span>
- <span data-ttu-id="1bde7-111">Управление клиентами направляется на один из этих URI на основе соответствующего уровня разрешений.</span><span class="sxs-lookup"><span data-stu-id="1bde7-111">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="1bde7-112">Например, клиент, которому предоставлено разрешение прослушивания, будет направлен на универсальный код ресурса (URI) для этого разрешения.</span><span class="sxs-lookup"><span data-stu-id="1bde7-112">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="1bde7-113">Удаление правила авторизации также приведет к удалению соответствующего разрешения пользователя.</span><span class="sxs-lookup"><span data-stu-id="1bde7-113">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="1bde7-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1bde7-114">EXAMPLES</span></span>

### <span data-ttu-id="1bde7-115">Пример 1: Удаление правила авторизации из центра уведомлений</span><span class="sxs-lookup"><span data-stu-id="1bde7-115">Example 1: Remove an authorization rule from a notification hub</span></span>
```
PS C:\>Remove-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -NotificationHub "ContosoExternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="1bde7-116">Эта команда удаляет правило авторизации с именем ListenRule из центра уведомлений с именем ContosoExternalHub.</span><span class="sxs-lookup"><span data-stu-id="1bde7-116">This command removes the authorization rule named ListenRule from the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="1bde7-117">При выполнении этой команды необходимо указать пространство имен и группу ресурсов, которым назначен концентратор.</span><span class="sxs-lookup"><span data-stu-id="1bde7-117">When you run this command you must specify both the namespace and the resource group that the hub is assigned to.</span></span>

## <span data-ttu-id="1bde7-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1bde7-118">PARAMETERS</span></span>

### <span data-ttu-id="1bde7-119">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1bde7-119">-AuthorizationRule</span></span>
<span data-ttu-id="1bde7-120">Указывает имя правила проверки подлинности SAS, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="1bde7-120">Specifies the name of the SAS authentication rule that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1bde7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bde7-121">-DefaultProfile</span></span>
<span data-ttu-id="1bde7-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1bde7-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1bde7-123">-Force</span><span class="sxs-lookup"><span data-stu-id="1bde7-123">-Force</span></span>
<span data-ttu-id="1bde7-124">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="1bde7-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="1bde7-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1bde7-125">-Namespace</span></span>
<span data-ttu-id="1bde7-126">Задает пространство имен, которому назначен Центр уведомлений.</span><span class="sxs-lookup"><span data-stu-id="1bde7-126">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="1bde7-127">Пространства имен обеспечивают способ группировки и классификации концентраторов уведомлений.</span><span class="sxs-lookup"><span data-stu-id="1bde7-127">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="1bde7-128">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="1bde7-128">-NotificationHub</span></span>
<span data-ttu-id="1bde7-129">Задает центр уведомлений, которому назначены правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="1bde7-129">Specifies the notification hub the authorization rules are assigned to.</span></span>
<span data-ttu-id="1bde7-130">Концентраторы уведомлений используются для отправки push-уведомлений нескольким клиентам вне зависимости от платформы.</span><span class="sxs-lookup"><span data-stu-id="1bde7-130">Notification hubs are used to send push notifications to multiple clients regardless of the platform.</span></span>

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

### <span data-ttu-id="1bde7-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1bde7-131">-ResourceGroup</span></span>
<span data-ttu-id="1bde7-132">Указывает группу ресурсов, которой назначен Центр уведомлений.</span><span class="sxs-lookup"><span data-stu-id="1bde7-132">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="1bde7-133">Группы ресурсов организуют элементы, такие как пространства имен, концентраторы уведомлений и правила авторизации, в целях простого управления запасами и администрирования Azure.</span><span class="sxs-lookup"><span data-stu-id="1bde7-133">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="1bde7-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1bde7-134">-Confirm</span></span>
<span data-ttu-id="1bde7-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1bde7-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bde7-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bde7-136">-WhatIf</span></span>
<span data-ttu-id="1bde7-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1bde7-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1bde7-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1bde7-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bde7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bde7-139">CommonParameters</span></span>
<span data-ttu-id="1bde7-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1bde7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bde7-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bde7-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bde7-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1bde7-142">INPUTS</span></span>

### <span data-ttu-id="1bde7-143">System. String</span><span class="sxs-lookup"><span data-stu-id="1bde7-143">System.String</span></span>

## <span data-ttu-id="1bde7-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1bde7-144">OUTPUTS</span></span>

### <span data-ttu-id="1bde7-145">System. void</span><span class="sxs-lookup"><span data-stu-id="1bde7-145">System.Void</span></span>

## <span data-ttu-id="1bde7-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="1bde7-146">NOTES</span></span>

## <span data-ttu-id="1bde7-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1bde7-147">RELATED LINKS</span></span>

[<span data-ttu-id="1bde7-148">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="1bde7-148">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="1bde7-149">New-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="1bde7-149">New-AzureRmNotificationHubAuthorizationRules</span></span>](./New-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="1bde7-150">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="1bde7-150">Set-AzureRmNotificationHubAuthorizationRules</span></span>](./Set-AzureRmNotificationHubAuthorizationRules.md)


