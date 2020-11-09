---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 860AB403-3F99-45FA-8E6A-8C9872C121E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: a25535e3aef21894091197d816c61f2aa5131df9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244042"
---
# <span data-ttu-id="9b365-101">Remove-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9b365-101">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="9b365-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9b365-102">SYNOPSIS</span></span>
<span data-ttu-id="9b365-103">Удаляет правило авторизации из пространства имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="9b365-103">Removes an authorization rule from a notification hub namespace.</span></span>

## <span data-ttu-id="9b365-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9b365-104">SYNTAX</span></span>

```
Remove-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9b365-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b365-105">DESCRIPTION</span></span>
<span data-ttu-id="9b365-106">Командлет **Remove-AzNotificationHubsNamespaceAuthorizationRule** удаляет правило авторизации для проверки подлинности общего доступа к подписи (SAS) из пространства имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="9b365-106">The **Remove-AzNotificationHubsNamespaceAuthorizationRule** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub namespace.</span></span>
<span data-ttu-id="9b365-107">Правила авторизации управляют доступом к пространству имен.</span><span class="sxs-lookup"><span data-stu-id="9b365-107">Authorization rules manage access to a namespace.</span></span>
<span data-ttu-id="9b365-108">Это делается посредством создания ссылок в виде URI, основанных на различных уровнях разрешений.</span><span class="sxs-lookup"><span data-stu-id="9b365-108">This is done by through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="9b365-109">Уровни разрешений могут быть следующими:</span><span class="sxs-lookup"><span data-stu-id="9b365-109">Permission levels can be of the following:</span></span> 
- <span data-ttu-id="9b365-110">Прослушивающих</span><span class="sxs-lookup"><span data-stu-id="9b365-110">Listen</span></span>
- <span data-ttu-id="9b365-111">Отправить</span><span class="sxs-lookup"><span data-stu-id="9b365-111">Send</span></span>
- <span data-ttu-id="9b365-112">Управление клиентами направляется на один из этих URI на основе соответствующего уровня разрешений.</span><span class="sxs-lookup"><span data-stu-id="9b365-112">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="9b365-113">Например, клиент, которому предоставлено разрешение прослушивания, перенаправляется на универсальный код ресурса (URI) для этого разрешения.</span><span class="sxs-lookup"><span data-stu-id="9b365-113">For instance, a client given the Listen permission is directed to the URI for that permission.</span></span>
<span data-ttu-id="9b365-114">Удаление правила авторизации также приведет к удалению соответствующего разрешения пользователя.</span><span class="sxs-lookup"><span data-stu-id="9b365-114">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="9b365-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9b365-115">EXAMPLES</span></span>

### <span data-ttu-id="9b365-116">Пример 1: Удаление правила авторизации из пространства имен</span><span class="sxs-lookup"><span data-stu-id="9b365-116">Example 1: Remove an authorization rule from a namespace</span></span>
```
PS C:\>Remove-AzNotificationHubNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="9b365-117">Эта команда удаляет правило авторизации с именем ListenRule из пространства имен с именем ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="9b365-117">This command removes the authorization rule named ListenRule from the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="9b365-118">При выполнении этой команды необходимо указать группу ресурсов, которой назначено пространство имен.</span><span class="sxs-lookup"><span data-stu-id="9b365-118">When you run this command you must specify the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="9b365-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9b365-119">PARAMETERS</span></span>

### <span data-ttu-id="9b365-120">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9b365-120">-AuthorizationRule</span></span>
<span data-ttu-id="9b365-121">Указывает имя удаляемого правила проверки подлинности SAS.</span><span class="sxs-lookup"><span data-stu-id="9b365-121">Specifies the name of the SAS authentication rule to be removed.</span></span>

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

### <span data-ttu-id="9b365-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b365-122">-DefaultProfile</span></span>
<span data-ttu-id="9b365-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9b365-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9b365-124">-Force</span><span class="sxs-lookup"><span data-stu-id="9b365-124">-Force</span></span>
<span data-ttu-id="9b365-125">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="9b365-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9b365-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9b365-126">-Namespace</span></span>
<span data-ttu-id="9b365-127">Задает пространство имен, которым назначены правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="9b365-127">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="9b365-128">Пространства имен обеспечивают способ группировки и классификации концентраторов уведомлений.</span><span class="sxs-lookup"><span data-stu-id="9b365-128">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="9b365-129">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9b365-129">-ResourceGroup</span></span>
<span data-ttu-id="9b365-130">Указывает группу ресурсов, которой назначено пространство имен.</span><span class="sxs-lookup"><span data-stu-id="9b365-130">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="9b365-131">Группы ресурсов организуют элементы, такие как пространства имен, концентраторы уведомлений и правила авторизации, в целях простого управления запасами и администрирования Azure.</span><span class="sxs-lookup"><span data-stu-id="9b365-131">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="9b365-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9b365-132">-Confirm</span></span>
<span data-ttu-id="9b365-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9b365-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b365-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b365-134">-WhatIf</span></span>
<span data-ttu-id="9b365-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9b365-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9b365-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9b365-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b365-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b365-137">CommonParameters</span></span>
<span data-ttu-id="9b365-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9b365-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b365-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b365-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b365-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9b365-140">INPUTS</span></span>

### <span data-ttu-id="9b365-141">System. String</span><span class="sxs-lookup"><span data-stu-id="9b365-141">System.String</span></span>

## <span data-ttu-id="9b365-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b365-142">OUTPUTS</span></span>

### <span data-ttu-id="9b365-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9b365-143">System.Boolean</span></span>

## <span data-ttu-id="9b365-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="9b365-144">NOTES</span></span>

## <span data-ttu-id="9b365-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9b365-145">RELATED LINKS</span></span>

[<span data-ttu-id="9b365-146">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9b365-146">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="9b365-147">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9b365-147">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./New-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="9b365-148">Set-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9b365-148">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Set-AzNotificationHubsNamespaceAuthorizationRule.md)

