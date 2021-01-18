---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 9805B3F1-C6BB-4A0F-A7C3-1DD1ACB75CDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
ms.openlocfilehash: 3d0e604d3984a40acde02fb1f977e2922ae2d1d7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517833"
---
# <span data-ttu-id="24b3d-101">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="24b3d-101">Get-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="24b3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24b3d-102">SYNOPSIS</span></span>
<span data-ttu-id="24b3d-103">Получает сведения о области имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="24b3d-103">Gets information about a notification hub namespace.</span></span>

## <span data-ttu-id="24b3d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="24b3d-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespace [[-ResourceGroup] <String>] [[-Namespace] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24b3d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="24b3d-105">DESCRIPTION</span></span>
<span data-ttu-id="24b3d-106">Чтобы получить сведения о пространствах имен концентратора уведомлений, можно получить сведения о **cmdlet Get-AzNotificationHubsNamespace.**</span><span class="sxs-lookup"><span data-stu-id="24b3d-106">**The Get-AzNotificationHubsNamespace** cmdlet gets information about notification hub namespaces.</span></span>
<span data-ttu-id="24b3d-107">Этот cmdlet обеспечивает получение сведений обо всех пространствах имен, а также об пространствах имен, которые назначены указанной группе ресурсов. или для получения сведений об определенном пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="24b3d-107">This cmdlet provides you the option of getting information for all your namespaces, information about the namespaces assigned to a specified resource group; or for returning information about a specific namespace.</span></span>
<span data-ttu-id="24b3d-108">Пространства имен — это логические контейнеры, которые помогают организовать концентраторы уведомлений и управлять ими.</span><span class="sxs-lookup"><span data-stu-id="24b3d-108">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="24b3d-109">Необходимо иметь хотя бы одно пространство имен концентратора уведомлений: все концентраторы уведомлений должны быть назначены для пространства имен.</span><span class="sxs-lookup"><span data-stu-id="24b3d-109">You must have at least one notification hub namespace: all notification hubs must be assigned to a namespace.</span></span>
<span data-ttu-id="24b3d-110">В одном пространстве имен может быть несколько концентраторов, что означает, что в вашей организации может потребоваться только одно пространство имен.</span><span class="sxs-lookup"><span data-stu-id="24b3d-110">A single namespace can house multiple hubs which means that you might only need one namespace in your organization.</span></span>
<span data-ttu-id="24b3d-111">Однако вы также можете использовать несколько пространства имен для более эффективного у упорядочества концентраторов или для того, чтобы предоставить определенным людям разрешение на управление выбранным подмножеством концентраторов.</span><span class="sxs-lookup"><span data-stu-id="24b3d-111">However, you can also have multiple namespaces to better organize your hubs, or to give specific individuals permission to manage a selected subset of hubs.</span></span>
<span data-ttu-id="24b3d-112">Для получения основных сведений о самом пространстве имен возвращается **cmdlet Get-AzNotificationHubsNamespace.**</span><span class="sxs-lookup"><span data-stu-id="24b3d-112">The **Get-AzNotificationHubsNamespace** cmdlet returns basic information about the namespace itself.</span></span>
<span data-ttu-id="24b3d-113">Чтобы получить сведения о правилах авторизации, связанных с пространством имен, используйте Get-AzNotificationHubsNamespaceAuthorizationRules.</span><span class="sxs-lookup"><span data-stu-id="24b3d-113">To get information about the authorization rules associated with a namespace use Get-AzNotificationHubsNamespaceAuthorizationRules.</span></span>

## <span data-ttu-id="24b3d-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="24b3d-114">EXAMPLES</span></span>

### <span data-ttu-id="24b3d-115">Пример 1. Получите сведения для всех пространства имен концентратора уведомлений</span><span class="sxs-lookup"><span data-stu-id="24b3d-115">Example 1: Get information for all notification hub namespaces</span></span>
```
PS C:\>Get-AzNotificationHubsNamespace
```

<span data-ttu-id="24b3d-116">Эта команда возвращает сведения для всех пространства имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="24b3d-116">This command returns information for all your notification hub namespaces.</span></span>

### <span data-ttu-id="24b3d-117">Пример 2. Получите сведения для одного пространства имен концентратора уведомлений</span><span class="sxs-lookup"><span data-stu-id="24b3d-117">Example 2: Get information for a single notification hub namespace</span></span>
```
PS C:\>Get-AzNotificationHubsNamespace -Namespace "ContosoNamespace"
```

<span data-ttu-id="24b3d-118">Эта команда получает сведения для единого пространства имен концентратора уведомлений: ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="24b3d-118">This command gets information for a single notification hub namespace: ContosoNamespace.</span></span>

### <span data-ttu-id="24b3d-119">Пример 3. Получить сведения для всех концентраторов уведомлений, которые назначены определенному пространству имен</span><span class="sxs-lookup"><span data-stu-id="24b3d-119">Example 3: Get information for all notification hubs assigned to a specific namespace</span></span>
```
PS C:\>Get-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="24b3d-120">Эта команда получает сведения для всех пространства имен концентратора уведомлений, которые назначены группе ресурсов ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="24b3d-120">This command gets information for all notification hub namespaces assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="24b3d-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24b3d-121">PARAMETERS</span></span>

### <span data-ttu-id="24b3d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24b3d-122">-DefaultProfile</span></span>
<span data-ttu-id="24b3d-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="24b3d-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="24b3d-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="24b3d-124">-Namespace</span></span>
<span data-ttu-id="24b3d-125">Указывает уникальное имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="24b3d-125">Specifies a unique name for the namespace.</span></span>
<span data-ttu-id="24b3d-126">Пространства имен предоставляют возможность группировать и классифицировать концентраторы уведомлений.</span><span class="sxs-lookup"><span data-stu-id="24b3d-126">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="24b3d-127">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="24b3d-127">-ResourceGroup</span></span>
<span data-ttu-id="24b3d-128">Группа ресурсов, которой назначено пространство имен.</span><span class="sxs-lookup"><span data-stu-id="24b3d-128">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="24b3d-129">Группы ресурсов упорядочиют такие элементы, как пространства имен, концентраторы уведомлений и правила авторизации, чтобы упрость управление запасами и администрирование Azure.</span><span class="sxs-lookup"><span data-stu-id="24b3d-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="24b3d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24b3d-130">CommonParameters</span></span>
<span data-ttu-id="24b3d-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24b3d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24b3d-132">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24b3d-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24b3d-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="24b3d-133">INPUTS</span></span>

### <span data-ttu-id="24b3d-134">System.String</span><span class="sxs-lookup"><span data-stu-id="24b3d-134">System.String</span></span>

## <span data-ttu-id="24b3d-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="24b3d-135">OUTPUTS</span></span>

### <span data-ttu-id="24b3d-136">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="24b3d-136">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="24b3d-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="24b3d-137">NOTES</span></span>

## <span data-ttu-id="24b3d-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="24b3d-138">RELATED LINKS</span></span>

[<span data-ttu-id="24b3d-139">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="24b3d-139">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="24b3d-140">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="24b3d-140">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="24b3d-141">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="24b3d-141">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)

[<span data-ttu-id="24b3d-142">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="24b3d-142">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


