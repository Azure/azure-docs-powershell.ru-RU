---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 62631E1C-FB43-4E87-82C2-159A9D1D4221
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHub.md
ms.openlocfilehash: 66f3dae7d92b9db18db418bf9de62671f084b7c0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246045"
---
# <span data-ttu-id="3e6de-101">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="3e6de-101">Remove-AzNotificationHub</span></span>

## <span data-ttu-id="3e6de-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3e6de-102">SYNOPSIS</span></span>
<span data-ttu-id="3e6de-103">Удаляет существующий концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3e6de-103">Removes an existing notification hub.</span></span>

## <span data-ttu-id="3e6de-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3e6de-104">SYNTAX</span></span>

```
Remove-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e6de-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e6de-105">DESCRIPTION</span></span>
<span data-ttu-id="3e6de-106">Командлет **Remove-AzNotificationHub** удаляет существующий концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3e6de-106">The **Remove-AzNotificationHub** cmdlet removes an existing notification hub.</span></span>
<span data-ttu-id="3e6de-107">Концентраторы уведомлений используются для отправки push-уведомлений нескольким клиентам вне зависимости от платформы, используемой этими клиентами.</span><span class="sxs-lookup"><span data-stu-id="3e6de-107">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="3e6de-108">Платформы включают, но не ограничиваются: iOS, Android, Windows Phone 8 и магазин Windows.</span><span class="sxs-lookup"><span data-stu-id="3e6de-108">Platforms include, but are not limited to: iOS, Android, Windows Phone 8, and Windows Store.</span></span>
<span data-ttu-id="3e6de-109">Концентраторы уведомлений примерно эквивалентны отдельным приложениям: каждое из ваших приложений обычно имеет собственный концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3e6de-109">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="3e6de-110">Вы можете удалить существующий центр уведомлений с помощью командлета **Remove-AzNotificationHub** .</span><span class="sxs-lookup"><span data-stu-id="3e6de-110">You can remove an existing notification hub by using the **Remove-AzNotificationHub** cmdlet.</span></span>
<span data-ttu-id="3e6de-111">После того как концентратор будет удален, вы больше не сможете использовать этот концентратор для отправки push-уведомлений пользователям.</span><span class="sxs-lookup"><span data-stu-id="3e6de-111">After a hub has been removed you can no longer use that hub to send push notifications to users.</span></span>

## <span data-ttu-id="3e6de-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3e6de-112">EXAMPLES</span></span>

### <span data-ttu-id="3e6de-113">Пример 1: удаление концентратора уведомлений</span><span class="sxs-lookup"><span data-stu-id="3e6de-113">Example 1: Remove a notification hub</span></span>
```
PS C:\>Remove-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="3e6de-114">Эта команда удаляет концентратор уведомлений с именем ContosoInternalHub.</span><span class="sxs-lookup"><span data-stu-id="3e6de-114">This command removes the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="3e6de-115">Для удаления концентратора необходимо указать пространство имен, в котором расположен концентратор, а также группу ресурсов, которой назначен концентратор.</span><span class="sxs-lookup"><span data-stu-id="3e6de-115">In order to remove the hub, you must specify the namespace where the hub is located as well as the resource group the hub is assigned to.</span></span>

## <span data-ttu-id="3e6de-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3e6de-116">PARAMETERS</span></span>

### <span data-ttu-id="3e6de-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e6de-117">-DefaultProfile</span></span>
<span data-ttu-id="3e6de-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3e6de-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3e6de-119">-Force</span><span class="sxs-lookup"><span data-stu-id="3e6de-119">-Force</span></span>
<span data-ttu-id="3e6de-120">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="3e6de-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="3e6de-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3e6de-121">-Namespace</span></span>
<span data-ttu-id="3e6de-122">Задает пространство имен, которому назначен Центр уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3e6de-122">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="3e6de-123">Пространства имен обеспечивают способ группировки и классификации концентраторов уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3e6de-123">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="3e6de-124">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="3e6de-124">-NotificationHub</span></span>
<span data-ttu-id="3e6de-125">Указывает удаляемый центр уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3e6de-125">Specifies the notification hub to be removed.</span></span>
<span data-ttu-id="3e6de-126">Концентраторы уведомлений используются для отправки push-уведомлений нескольким клиентам вне зависимости от платформы, используемой этими клиентами.</span><span class="sxs-lookup"><span data-stu-id="3e6de-126">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="3e6de-127">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3e6de-127">-ResourceGroup</span></span>
<span data-ttu-id="3e6de-128">Указывает группу ресурсов, которой назначен Центр уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3e6de-128">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="3e6de-129">Группы ресурсов организуют элементы, такие как пространства имен, концентраторы уведомлений и правила авторизации, в целях простого управления запасами и администрирования Azure.</span><span class="sxs-lookup"><span data-stu-id="3e6de-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="3e6de-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3e6de-130">-Confirm</span></span>
<span data-ttu-id="3e6de-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3e6de-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e6de-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e6de-132">-WhatIf</span></span>
<span data-ttu-id="3e6de-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3e6de-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3e6de-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3e6de-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e6de-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e6de-135">CommonParameters</span></span>
<span data-ttu-id="3e6de-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3e6de-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e6de-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e6de-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e6de-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3e6de-138">INPUTS</span></span>

### <span data-ttu-id="3e6de-139">System. String</span><span class="sxs-lookup"><span data-stu-id="3e6de-139">System.String</span></span>

## <span data-ttu-id="3e6de-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e6de-140">OUTPUTS</span></span>

### <span data-ttu-id="3e6de-141">System. void</span><span class="sxs-lookup"><span data-stu-id="3e6de-141">System.Void</span></span>

## <span data-ttu-id="3e6de-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="3e6de-142">NOTES</span></span>

## <span data-ttu-id="3e6de-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3e6de-143">RELATED LINKS</span></span>

[<span data-ttu-id="3e6de-144">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="3e6de-144">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="3e6de-145">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="3e6de-145">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="3e6de-146">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="3e6de-146">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)


