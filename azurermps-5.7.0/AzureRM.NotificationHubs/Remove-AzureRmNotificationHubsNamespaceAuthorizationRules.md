---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 860AB403-3F99-45FA-8E6A-8C9872C121E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/remove-azurermnotificationhubsnamespaceauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: eee4d9db5cbc64f8ae7e17f18026f5bd2aeca310
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734976"
---
# <span data-ttu-id="35eb9-101">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="35eb9-101">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>

## <span data-ttu-id="35eb9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="35eb9-102">SYNOPSIS</span></span>
<span data-ttu-id="35eb9-103">Удаляет правило авторизации из пространства имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="35eb9-103">Removes an authorization rule from a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35eb9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="35eb9-104">SYNTAX</span></span>

```
Remove-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="35eb9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="35eb9-105">DESCRIPTION</span></span>
<span data-ttu-id="35eb9-106">Командлет **Remove-AzureRmNotificationHubsNamespaceAuthorizationRules** удаляет правило авторизации для проверки подлинности общего доступа к подписи (SAS) из пространства имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="35eb9-106">The **Remove-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub namespace.</span></span>

<span data-ttu-id="35eb9-107">Правила авторизации управляют доступом к пространству имен.</span><span class="sxs-lookup"><span data-stu-id="35eb9-107">Authorization rules manage access to a namespace.</span></span>
<span data-ttu-id="35eb9-108">Это делается посредством создания ссылок в виде URI, основанных на различных уровнях разрешений.</span><span class="sxs-lookup"><span data-stu-id="35eb9-108">This is done by through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="35eb9-109">Уровни разрешений могут быть следующими:</span><span class="sxs-lookup"><span data-stu-id="35eb9-109">Permission levels can be of the following:</span></span> 

- <span data-ttu-id="35eb9-110">Прослушивающих</span><span class="sxs-lookup"><span data-stu-id="35eb9-110">Listen</span></span>
- <span data-ttu-id="35eb9-111">Отправить</span><span class="sxs-lookup"><span data-stu-id="35eb9-111">Send</span></span>
- <span data-ttu-id="35eb9-112">Этими</span><span class="sxs-lookup"><span data-stu-id="35eb9-112">Manage</span></span>

<span data-ttu-id="35eb9-113">Клиенты направляются на один из этих URI на основе соответствующего уровня разрешений.</span><span class="sxs-lookup"><span data-stu-id="35eb9-113">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="35eb9-114">Например, клиент, которому предоставлено разрешение прослушивания, перенаправляется на универсальный код ресурса (URI) для этого разрешения.</span><span class="sxs-lookup"><span data-stu-id="35eb9-114">For instance, a client given the Listen permission is directed to the URI for that permission.</span></span>

<span data-ttu-id="35eb9-115">Удаление правила авторизации также приведет к удалению соответствующего разрешения пользователя.</span><span class="sxs-lookup"><span data-stu-id="35eb9-115">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="35eb9-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="35eb9-116">EXAMPLES</span></span>

### <span data-ttu-id="35eb9-117">Пример 1: Удаление правила авторизации из пространства имен</span><span class="sxs-lookup"><span data-stu-id="35eb9-117">Example 1: Remove an authorization rule from a namespace</span></span>
```
PS C:\>Remove-AzureRmNotificationHubNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="35eb9-118">Эта команда удаляет правило авторизации с именем ListenRule из пространства имен с именем ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="35eb9-118">This command removes the authorization rule named ListenRule from the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="35eb9-119">При выполнении этой команды необходимо указать группу ресурсов, которой назначено пространство имен.</span><span class="sxs-lookup"><span data-stu-id="35eb9-119">When you run this command you must specify the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="35eb9-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="35eb9-120">PARAMETERS</span></span>

### <span data-ttu-id="35eb9-121">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="35eb9-121">-AuthorizationRule</span></span>
<span data-ttu-id="35eb9-122">Указывает имя удаляемого правила проверки подлинности SAS.</span><span class="sxs-lookup"><span data-stu-id="35eb9-122">Specifies the name of the SAS authentication rule to be removed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35eb9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35eb9-123">-DefaultProfile</span></span>
<span data-ttu-id="35eb9-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="35eb9-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="35eb9-125">-Force</span><span class="sxs-lookup"><span data-stu-id="35eb9-125">-Force</span></span>
<span data-ttu-id="35eb9-126">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="35eb9-126">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35eb9-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="35eb9-127">-Namespace</span></span>
<span data-ttu-id="35eb9-128">Задает пространство имен, которым назначены правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="35eb9-128">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="35eb9-129">Пространства имен обеспечивают способ группировки и классификации концентраторов уведомлений.</span><span class="sxs-lookup"><span data-stu-id="35eb9-129">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="35eb9-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="35eb9-130">-ResourceGroup</span></span>
<span data-ttu-id="35eb9-131">Указывает группу ресурсов, которой назначено пространство имен.</span><span class="sxs-lookup"><span data-stu-id="35eb9-131">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="35eb9-132">Группы ресурсов организуют элементы, такие как пространства имен, концентраторы уведомлений и правила авторизации, в целях простого управления запасами и администрирования Azure.</span><span class="sxs-lookup"><span data-stu-id="35eb9-132">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="35eb9-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35eb9-133">-Confirm</span></span>
<span data-ttu-id="35eb9-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="35eb9-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35eb9-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35eb9-135">-WhatIf</span></span>
<span data-ttu-id="35eb9-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="35eb9-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="35eb9-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="35eb9-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35eb9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35eb9-138">CommonParameters</span></span>
<span data-ttu-id="35eb9-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="35eb9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35eb9-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35eb9-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35eb9-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="35eb9-141">INPUTS</span></span>

### <span data-ttu-id="35eb9-142">Ничего</span><span class="sxs-lookup"><span data-stu-id="35eb9-142">None</span></span>
<span data-ttu-id="35eb9-143">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="35eb9-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="35eb9-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="35eb9-144">OUTPUTS</span></span>

### <span data-ttu-id="35eb9-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="35eb9-145">System.Boolean</span></span>

## <span data-ttu-id="35eb9-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="35eb9-146">NOTES</span></span>

## <span data-ttu-id="35eb9-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="35eb9-147">RELATED LINKS</span></span>

[<span data-ttu-id="35eb9-148">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="35eb9-148">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="35eb9-149">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="35eb9-149">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./New-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="35eb9-150">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="35eb9-150">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Set-AzureRmNotificationHubsNamespaceAuthorizationRules.md)


