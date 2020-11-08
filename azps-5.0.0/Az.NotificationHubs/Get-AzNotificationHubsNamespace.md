---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 9805B3F1-C6BB-4A0F-A7C3-1DD1ACB75CDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
ms.openlocfilehash: 3d0e604d3984a40acde02fb1f977e2922ae2d1d7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246054"
---
# <span data-ttu-id="ebe61-101">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="ebe61-101">Get-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="ebe61-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ebe61-102">SYNOPSIS</span></span>
<span data-ttu-id="ebe61-103">Получает сведения о пространстве имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="ebe61-103">Gets information about a notification hub namespace.</span></span>

## <span data-ttu-id="ebe61-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ebe61-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespace [[-ResourceGroup] <String>] [[-Namespace] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ebe61-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebe61-105">DESCRIPTION</span></span>
<span data-ttu-id="ebe61-106">Командлет **Get-AzNotificationHubsNamespace** получает сведения о пространствах имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="ebe61-106">**The Get-AzNotificationHubsNamespace** cmdlet gets information about notification hub namespaces.</span></span>
<span data-ttu-id="ebe61-107">Этот командлет предоставляет возможность получения сведений обо всех пространствах имен, а также сведения о пространствах имен, назначенных определенной группе ресурсов; или для возврата сведений о конкретном пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="ebe61-107">This cmdlet provides you the option of getting information for all your namespaces, information about the namespaces assigned to a specified resource group; or for returning information about a specific namespace.</span></span>
<span data-ttu-id="ebe61-108">Пространства имен — это логические контейнеры, помогающие упорядочивать концентраторы уведомлений и управлять ими.</span><span class="sxs-lookup"><span data-stu-id="ebe61-108">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="ebe61-109">Необходимо иметь по крайней мере одно пространство имен концентратора уведомлений: все концентраторы уведомлений должны быть назначены пространству имен.</span><span class="sxs-lookup"><span data-stu-id="ebe61-109">You must have at least one notification hub namespace: all notification hubs must be assigned to a namespace.</span></span>
<span data-ttu-id="ebe61-110">Одно пространство имен может быть размещено на нескольких концентраторах, что означает, что вам потребуется только одно пространство имен в Организации.</span><span class="sxs-lookup"><span data-stu-id="ebe61-110">A single namespace can house multiple hubs which means that you might only need one namespace in your organization.</span></span>
<span data-ttu-id="ebe61-111">Однако вы также можете использовать несколько пространств имен для более эффективной организации концентраторов или предоставить конкретным пользователям разрешение на управление выбранной подмножеством концентраторов.</span><span class="sxs-lookup"><span data-stu-id="ebe61-111">However, you can also have multiple namespaces to better organize your hubs, or to give specific individuals permission to manage a selected subset of hubs.</span></span>
<span data-ttu-id="ebe61-112">Командлет **Get-AzNotificationHubsNamespace** возвращает основные сведения о пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="ebe61-112">The **Get-AzNotificationHubsNamespace** cmdlet returns basic information about the namespace itself.</span></span>
<span data-ttu-id="ebe61-113">Чтобы получить сведения о правилах авторизации, связанных с пространством имен, используйте Get-AzNotificationHubsNamespaceAuthorizationRules.</span><span class="sxs-lookup"><span data-stu-id="ebe61-113">To get information about the authorization rules associated with a namespace use Get-AzNotificationHubsNamespaceAuthorizationRules.</span></span>

## <span data-ttu-id="ebe61-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ebe61-114">EXAMPLES</span></span>

### <span data-ttu-id="ebe61-115">Пример 1: получение сведений для всех пространств имен концентратора уведомлений</span><span class="sxs-lookup"><span data-stu-id="ebe61-115">Example 1: Get information for all notification hub namespaces</span></span>
```
PS C:\>Get-AzNotificationHubsNamespace
```

<span data-ttu-id="ebe61-116">Эта команда возвращает сведения обо всех пространствах имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="ebe61-116">This command returns information for all your notification hub namespaces.</span></span>

### <span data-ttu-id="ebe61-117">Пример 2: получение сведений для одного пространства имен концентратора уведомлений</span><span class="sxs-lookup"><span data-stu-id="ebe61-117">Example 2: Get information for a single notification hub namespace</span></span>
```
PS C:\>Get-AzNotificationHubsNamespace -Namespace "ContosoNamespace"
```

<span data-ttu-id="ebe61-118">Эта команда получает сведения для одного пространства имен концентратора уведомлений: ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="ebe61-118">This command gets information for a single notification hub namespace: ContosoNamespace.</span></span>

### <span data-ttu-id="ebe61-119">Пример 3: получение сведений для всех концентраторов уведомлений, назначенных определенному пространству имен</span><span class="sxs-lookup"><span data-stu-id="ebe61-119">Example 3: Get information for all notification hubs assigned to a specific namespace</span></span>
```
PS C:\>Get-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="ebe61-120">Эта команда получает сведения обо всех пространствах имен концентратора уведомлений, назначенных группе ресурсов ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="ebe61-120">This command gets information for all notification hub namespaces assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="ebe61-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ebe61-121">PARAMETERS</span></span>

### <span data-ttu-id="ebe61-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebe61-122">-DefaultProfile</span></span>
<span data-ttu-id="ebe61-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ebe61-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ebe61-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ebe61-124">-Namespace</span></span>
<span data-ttu-id="ebe61-125">Задает уникальное имя для пространства имен.</span><span class="sxs-lookup"><span data-stu-id="ebe61-125">Specifies a unique name for the namespace.</span></span>
<span data-ttu-id="ebe61-126">Пространства имен обеспечивают способ группировки и классификации концентраторов уведомлений.</span><span class="sxs-lookup"><span data-stu-id="ebe61-126">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebe61-127">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ebe61-127">-ResourceGroup</span></span>
<span data-ttu-id="ebe61-128">Указывает группу ресурсов, которой назначено пространство имен.</span><span class="sxs-lookup"><span data-stu-id="ebe61-128">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="ebe61-129">Группы ресурсов организуют элементы, такие как пространства имен, концентраторы уведомлений и правила авторизации, в целях простого управления запасами и администрирования Azure.</span><span class="sxs-lookup"><span data-stu-id="ebe61-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebe61-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebe61-130">CommonParameters</span></span>
<span data-ttu-id="ebe61-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ebe61-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebe61-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebe61-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebe61-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ebe61-133">INPUTS</span></span>

### <span data-ttu-id="ebe61-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ebe61-134">System.String</span></span>

## <span data-ttu-id="ebe61-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebe61-135">OUTPUTS</span></span>

### <span data-ttu-id="ebe61-136">Microsoft. Azure. Commands. NotificationHubs. Models. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="ebe61-136">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="ebe61-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="ebe61-137">NOTES</span></span>

## <span data-ttu-id="ebe61-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ebe61-138">RELATED LINKS</span></span>

[<span data-ttu-id="ebe61-139">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ebe61-139">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="ebe61-140">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="ebe61-140">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="ebe61-141">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="ebe61-141">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)

[<span data-ttu-id="ebe61-142">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="ebe61-142">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


