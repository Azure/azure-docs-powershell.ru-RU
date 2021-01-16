---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 5EDFBF19-928F-4F95-BD93-CF8BAEA11C52
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespace.md
ms.openlocfilehash: e03be5a1daae753e1538b171586d9a8e46ad8021
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404871"
---
# <span data-ttu-id="8a5c1-101">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="8a5c1-101">Remove-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="8a5c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a5c1-102">SYNOPSIS</span></span>
<span data-ttu-id="8a5c1-103">Удаляет пространство имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="8a5c1-103">Removes a notification hub namespace.</span></span>

## <span data-ttu-id="8a5c1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8a5c1-104">SYNTAX</span></span>

```
Remove-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a5c1-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a5c1-105">DESCRIPTION</span></span>
<span data-ttu-id="8a5c1-106">При **развертывании удаляется** пространство имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="8a5c1-106">The **Remove-AzNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="8a5c1-107">Пространства имен — это логические контейнеры, которые помогают организовать концентраторы уведомлений и управлять ими.</span><span class="sxs-lookup"><span data-stu-id="8a5c1-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="8a5c1-108">При **развертывании удаляется** пространство имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="8a5c1-108">The **Remove-AzNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="8a5c1-109">При запуске этого cmdlet указанное пространство имен удаляется вместе со всеми центрами уведомлений, связанными с этим пространством имен.</span><span class="sxs-lookup"><span data-stu-id="8a5c1-109">When you run this cmdlet, the specified namespace will be deleted along with all the notification hubs associated with that namespace.</span></span>

## <span data-ttu-id="8a5c1-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8a5c1-110">EXAMPLES</span></span>

### <span data-ttu-id="8a5c1-111">Пример 1. Удаление пространства имен концентратора уведомлений</span><span class="sxs-lookup"><span data-stu-id="8a5c1-111">Example 1: Remove a notification hub namespace</span></span>
```
PS C:\>Remove-AzNotificationHubsNamespace -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="8a5c1-112">Эта команда удаляет пространство имен с именем ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="8a5c1-112">This command removes the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="8a5c1-113">Необходимо указать группу ресурсов, которая назначена области имен.</span><span class="sxs-lookup"><span data-stu-id="8a5c1-113">You must specify the resource group the namespace is assigned to.</span></span>

## <span data-ttu-id="8a5c1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8a5c1-114">PARAMETERS</span></span>

### <span data-ttu-id="8a5c1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a5c1-115">-DefaultProfile</span></span>
<span data-ttu-id="8a5c1-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8a5c1-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8a5c1-117">-Force</span><span class="sxs-lookup"><span data-stu-id="8a5c1-117">-Force</span></span>
<span data-ttu-id="8a5c1-118">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="8a5c1-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8a5c1-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8a5c1-119">-Namespace</span></span>
<span data-ttu-id="8a5c1-120">Определяет пространство имен, которое удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a5c1-120">Specifies the namespace that this cmdlet removes.</span></span>
<span data-ttu-id="8a5c1-121">Пространства имен предоставляют возможность группировать и классифицировать концентраторы уведомлений.</span><span class="sxs-lookup"><span data-stu-id="8a5c1-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="8a5c1-122">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8a5c1-122">-ResourceGroup</span></span>
<span data-ttu-id="8a5c1-123">Группа ресурсов, которой назначено пространство имен.</span><span class="sxs-lookup"><span data-stu-id="8a5c1-123">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="8a5c1-124">Группы ресурсов упорядочиют такие элементы, как пространства имен, концентраторы уведомлений и правила авторизации, чтобы упрость управление запасами и администрирование Azure.</span><span class="sxs-lookup"><span data-stu-id="8a5c1-124">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="8a5c1-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8a5c1-125">-Confirm</span></span>
<span data-ttu-id="8a5c1-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a5c1-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a5c1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a5c1-127">-WhatIf</span></span>
<span data-ttu-id="8a5c1-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a5c1-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8a5c1-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8a5c1-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a5c1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a5c1-130">CommonParameters</span></span>
<span data-ttu-id="8a5c1-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a5c1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a5c1-132">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a5c1-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a5c1-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8a5c1-133">INPUTS</span></span>

### <span data-ttu-id="8a5c1-134">System.String</span><span class="sxs-lookup"><span data-stu-id="8a5c1-134">System.String</span></span>

## <span data-ttu-id="8a5c1-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8a5c1-135">OUTPUTS</span></span>

### <span data-ttu-id="8a5c1-136">System.Void</span><span class="sxs-lookup"><span data-stu-id="8a5c1-136">System.Void</span></span>

## <span data-ttu-id="8a5c1-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8a5c1-137">NOTES</span></span>

## <span data-ttu-id="8a5c1-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8a5c1-138">RELATED LINKS</span></span>

[<span data-ttu-id="8a5c1-139">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="8a5c1-139">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="8a5c1-140">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="8a5c1-140">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="8a5c1-141">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="8a5c1-141">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


