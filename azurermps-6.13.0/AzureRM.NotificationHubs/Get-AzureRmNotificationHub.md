---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHub.md
ms.openlocfilehash: af2cc43b5f70c8a892e8b8fad0177a804689f007
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565828"
---
# <span data-ttu-id="a8ac1-101">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="a8ac1-101">Get-AzureRmNotificationHub</span></span>

## <span data-ttu-id="a8ac1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a8ac1-102">SYNOPSIS</span></span>
<span data-ttu-id="a8ac1-103">Получение сведений о концентраторах уведомлений.</span><span class="sxs-lookup"><span data-stu-id="a8ac1-103">Gets information about your notification hubs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8ac1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a8ac1-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8ac1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8ac1-105">DESCRIPTION</span></span>
<span data-ttu-id="a8ac1-106">Командлет **Get-AzureRmNotificationHub** получает сведения о концентраторах уведомлений в указанном пространстве имен и назначенных определенной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a8ac1-106">The **Get-AzureRmNotificationHub** cmdlet gets information about the notification hubs in a specified namespace and assigned to a specified resource group.</span></span>
<span data-ttu-id="a8ac1-107">Например, вы можете получить сведения обо всех концентраторах уведомлений в пространстве имен ContosoNamespace и назначить группе ресурсов ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="a8ac1-107">For example, you can get information for all the notification hubs in the namespace ContosoNamespace and assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="a8ac1-108">Кроме того, можно использовать параметр *NotificationHub* для ограничения возвращенных данных сведениями об определенном концентраторе уведомлений.</span><span class="sxs-lookup"><span data-stu-id="a8ac1-108">Alternatively, you can use the *NotificationHub* parameter to limit the returned data to information about a specific notification hub.</span></span>
<span data-ttu-id="a8ac1-109">Концентраторы уведомлений используются для отправки push-уведомлений нескольким клиентам вне зависимости от платформы, например iOS, Android, Windows Phone 8 и магазина Windows, используемой этими клиентами.</span><span class="sxs-lookup"><span data-stu-id="a8ac1-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform, such as iOS, Android, Windows Phone 8, and Windows Store, used by those clients.</span></span>
<span data-ttu-id="a8ac1-110">Эти разветвители примерно эквивалентны отдельным приложениям, и каждое из ваших приложений обычно имеет собственный концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="a8ac1-110">These hubs are roughly equivalent to individual apps and each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="a8ac1-111">Этот командлет получает сведения только о самом концентраторе.</span><span class="sxs-lookup"><span data-stu-id="a8ac1-111">This cmdlet only gets information about the hub itself.</span></span>
<span data-ttu-id="a8ac1-112">Другие командлеты, такие как Get-AzureRmNotificationHubAuthorizationRules, Get-AzureRmNotificationHubListKeys и Get-AzureRmNotificationHubPNSCredentials, необходимы для получения сведений о правилах авторизации концентратора, строках подключения и учетных данных службы уведомлений платформы.</span><span class="sxs-lookup"><span data-stu-id="a8ac1-112">Other cmdlets, such as Get-AzureRmNotificationHubAuthorizationRules, Get-AzureRmNotificationHubListKeys, and Get-AzureRmNotificationHubPNSCredentials, are needed to get information about a hub's authorization rules, connection strings, and platform notification service credentials.</span></span>

## <span data-ttu-id="a8ac1-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a8ac1-113">EXAMPLES</span></span>

### <span data-ttu-id="a8ac1-114">Пример 1: получение сведений для всех концентраторов уведомлений в определенном пространстве имен</span><span class="sxs-lookup"><span data-stu-id="a8ac1-114">Example 1: Get information for all notification hubs in a specific namespace</span></span>
```
PS C:\>Get-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="a8ac1-115">Эта команда получает сведения для всех концентраторов уведомлений в пространстве имен с именем ContosoNamespace, назначенных группе ресурсов ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="a8ac1-115">This command gets information for all the notification hubs in the namespace named ContosoNamespace that have been assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="a8ac1-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a8ac1-116">PARAMETERS</span></span>

### <span data-ttu-id="a8ac1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8ac1-117">-DefaultProfile</span></span>
<span data-ttu-id="a8ac1-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a8ac1-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a8ac1-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a8ac1-119">-Namespace</span></span>
<span data-ttu-id="a8ac1-120">Задает пространство имен, которому назначен Центр уведомлений.</span><span class="sxs-lookup"><span data-stu-id="a8ac1-120">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="a8ac1-121">Пространства имен обеспечивают способ группировки и классификации концентраторов уведомлений.</span><span class="sxs-lookup"><span data-stu-id="a8ac1-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="a8ac1-122">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="a8ac1-122">-NotificationHub</span></span>
<span data-ttu-id="a8ac1-123">Указывает имя центра уведомлений, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a8ac1-123">Specifies the name of the notification hub that this cmdlet gets.</span></span>
<span data-ttu-id="a8ac1-124">Концентраторы уведомлений используются для отправки push-уведомлений нескольким клиентам вне зависимости от платформы, используемой этими клиентами.</span><span class="sxs-lookup"><span data-stu-id="a8ac1-124">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8ac1-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a8ac1-125">-ResourceGroup</span></span>
<span data-ttu-id="a8ac1-126">Указывает группу ресурсов, которой назначен Центр уведомлений.</span><span class="sxs-lookup"><span data-stu-id="a8ac1-126">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="a8ac1-127">Группы ресурсов организуют элементы, такие как пространства имен, концентраторы уведомлений и правила авторизации, в целях простого управления запасами и администрирования Azure.</span><span class="sxs-lookup"><span data-stu-id="a8ac1-127">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="a8ac1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8ac1-128">CommonParameters</span></span>
<span data-ttu-id="a8ac1-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a8ac1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8ac1-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8ac1-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8ac1-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a8ac1-131">INPUTS</span></span>

### <span data-ttu-id="a8ac1-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a8ac1-132">System.String</span></span>

## <span data-ttu-id="a8ac1-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8ac1-133">OUTPUTS</span></span>

### <span data-ttu-id="a8ac1-134">Microsoft. Azure. Commands. NotificationHubs. Models. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="a8ac1-134">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="a8ac1-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="a8ac1-135">NOTES</span></span>

## <span data-ttu-id="a8ac1-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a8ac1-136">RELATED LINKS</span></span>

[<span data-ttu-id="a8ac1-137">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="a8ac1-137">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="a8ac1-138">Get-AzureRmNotificationHubListKeys</span><span class="sxs-lookup"><span data-stu-id="a8ac1-138">Get-AzureRmNotificationHubListKeys</span></span>](./Get-AzureRmNotificationHubListKeys.md)

[<span data-ttu-id="a8ac1-139">Get-AzureRmNotificationHubPNSCredentials</span><span class="sxs-lookup"><span data-stu-id="a8ac1-139">Get-AzureRmNotificationHubPNSCredentials</span></span>](./Get-AzureRmNotificationHubPNSCredentials.md)

[<span data-ttu-id="a8ac1-140">New-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="a8ac1-140">New-AzureRmNotificationHub</span></span>](./New-AzureRmNotificationHub.md)

[<span data-ttu-id="a8ac1-141">Remove-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="a8ac1-141">Remove-AzureRmNotificationHub</span></span>](./Remove-AzureRmNotificationHub.md)

[<span data-ttu-id="a8ac1-142">Set-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="a8ac1-142">Set-AzureRmNotificationHub</span></span>](./Set-AzureRmNotificationHub.md)


