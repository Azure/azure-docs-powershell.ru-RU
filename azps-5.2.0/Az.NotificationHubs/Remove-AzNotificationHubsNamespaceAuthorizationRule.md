---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 860AB403-3F99-45FA-8E6A-8C9872C121E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: a25535e3aef21894091197d816c61f2aa5131df9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395228"
---
# <span data-ttu-id="8f4be-101">Remove-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="8f4be-101">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="8f4be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f4be-102">SYNOPSIS</span></span>
<span data-ttu-id="8f4be-103">Удаляет правило авторизации из пространства имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="8f4be-103">Removes an authorization rule from a notification hub namespace.</span></span>

## <span data-ttu-id="8f4be-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8f4be-104">SYNTAX</span></span>

```
Remove-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8f4be-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f4be-105">DESCRIPTION</span></span>
<span data-ttu-id="8f4be-106">При этом правило авторизации **Remove-AzNotificationHubsNamespaceAuthorizationRule** удаляет правило авторизации saS из пространства имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="8f4be-106">The **Remove-AzNotificationHubsNamespaceAuthorizationRule** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub namespace.</span></span>
<span data-ttu-id="8f4be-107">Правила авторизации управляют доступом к пространству имен.</span><span class="sxs-lookup"><span data-stu-id="8f4be-107">Authorization rules manage access to a namespace.</span></span>
<span data-ttu-id="8f4be-108">Для этого нужно создать ссылки ( URIS) на основе различных уровней разрешений.</span><span class="sxs-lookup"><span data-stu-id="8f4be-108">This is done by through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="8f4be-109">Уровни разрешений могут быть следующими:</span><span class="sxs-lookup"><span data-stu-id="8f4be-109">Permission levels can be of the following:</span></span> 
- <span data-ttu-id="8f4be-110">Прослушивание</span><span class="sxs-lookup"><span data-stu-id="8f4be-110">Listen</span></span>
- <span data-ttu-id="8f4be-111">Отправить</span><span class="sxs-lookup"><span data-stu-id="8f4be-111">Send</span></span>
- <span data-ttu-id="8f4be-112">Управление клиентами направляется на один из этих ЮРИСов с учетом соответствующего уровня разрешений.</span><span class="sxs-lookup"><span data-stu-id="8f4be-112">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="8f4be-113">Например, клиент с разрешением на прослушивание направляется в URI для этого разрешения.</span><span class="sxs-lookup"><span data-stu-id="8f4be-113">For instance, a client given the Listen permission is directed to the URI for that permission.</span></span>
<span data-ttu-id="8f4be-114">При удалении правила авторизации также удаляется соответствующее разрешение пользователя.</span><span class="sxs-lookup"><span data-stu-id="8f4be-114">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="8f4be-115">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8f4be-115">EXAMPLES</span></span>

### <span data-ttu-id="8f4be-116">Пример 1. Удаление правила авторизации из пространства имен</span><span class="sxs-lookup"><span data-stu-id="8f4be-116">Example 1: Remove an authorization rule from a namespace</span></span>
```
PS C:\>Remove-AzNotificationHubNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="8f4be-117">Эта команда удаляет правило авторизации listenRule из пространства имен с именем ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="8f4be-117">This command removes the authorization rule named ListenRule from the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="8f4be-118">При запуске этой команды необходимо указать группу ресурсов, которая назначена области имен.</span><span class="sxs-lookup"><span data-stu-id="8f4be-118">When you run this command you must specify the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="8f4be-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f4be-119">PARAMETERS</span></span>

### <span data-ttu-id="8f4be-120">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="8f4be-120">-AuthorizationRule</span></span>
<span data-ttu-id="8f4be-121">Имя удаляемого правила проверки подлинности SAS.</span><span class="sxs-lookup"><span data-stu-id="8f4be-121">Specifies the name of the SAS authentication rule to be removed.</span></span>

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

### <span data-ttu-id="8f4be-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f4be-122">-DefaultProfile</span></span>
<span data-ttu-id="8f4be-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8f4be-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f4be-124">-Force</span><span class="sxs-lookup"><span data-stu-id="8f4be-124">-Force</span></span>
<span data-ttu-id="8f4be-125">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="8f4be-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8f4be-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8f4be-126">-Namespace</span></span>
<span data-ttu-id="8f4be-127">Определяет пространство имен, которому назначены правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="8f4be-127">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="8f4be-128">Пространства имен предоставляют возможность группировать концентраторы уведомлений и классифицировать их.</span><span class="sxs-lookup"><span data-stu-id="8f4be-128">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="8f4be-129">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8f4be-129">-ResourceGroup</span></span>
<span data-ttu-id="8f4be-130">Группа ресурсов, которой назначено пространство имен.</span><span class="sxs-lookup"><span data-stu-id="8f4be-130">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="8f4be-131">Группы ресурсов упорядочиют такие элементы, как пространства имен, концентраторы уведомлений и правила авторизации, чтобы упрость управление запасами и администрирование Azure.</span><span class="sxs-lookup"><span data-stu-id="8f4be-131">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="8f4be-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8f4be-132">-Confirm</span></span>
<span data-ttu-id="8f4be-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="8f4be-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f4be-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f4be-134">-WhatIf</span></span>
<span data-ttu-id="8f4be-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f4be-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8f4be-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8f4be-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f4be-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f4be-137">CommonParameters</span></span>
<span data-ttu-id="8f4be-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f4be-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f4be-139">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f4be-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f4be-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8f4be-140">INPUTS</span></span>

### <span data-ttu-id="8f4be-141">System.String</span><span class="sxs-lookup"><span data-stu-id="8f4be-141">System.String</span></span>

## <span data-ttu-id="8f4be-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8f4be-142">OUTPUTS</span></span>

### <span data-ttu-id="8f4be-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8f4be-143">System.Boolean</span></span>

## <span data-ttu-id="8f4be-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8f4be-144">NOTES</span></span>

## <span data-ttu-id="8f4be-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8f4be-145">RELATED LINKS</span></span>

[<span data-ttu-id="8f4be-146">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="8f4be-146">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="8f4be-147">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="8f4be-147">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./New-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="8f4be-148">Set-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="8f4be-148">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Set-AzNotificationHubsNamespaceAuthorizationRule.md)


