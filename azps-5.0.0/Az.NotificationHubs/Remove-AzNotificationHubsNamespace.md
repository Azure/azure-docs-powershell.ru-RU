---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 5EDFBF19-928F-4F95-BD93-CF8BAEA11C52
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespace.md
ms.openlocfilehash: e03be5a1daae753e1538b171586d9a8e46ad8021
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316575"
---
# <span data-ttu-id="ea2d8-101">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="ea2d8-101">Remove-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="ea2d8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ea2d8-102">SYNOPSIS</span></span>
<span data-ttu-id="ea2d8-103">Удаляет пространство имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="ea2d8-103">Removes a notification hub namespace.</span></span>

## <span data-ttu-id="ea2d8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ea2d8-104">SYNTAX</span></span>

```
Remove-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea2d8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea2d8-105">DESCRIPTION</span></span>
<span data-ttu-id="ea2d8-106">Командлет **Remove-AzNotificationHubsNamespace** удаляет пространство имен концентратора уведомлений из развертывания.</span><span class="sxs-lookup"><span data-stu-id="ea2d8-106">The **Remove-AzNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="ea2d8-107">Пространства имен — это логические контейнеры, помогающие упорядочивать концентраторы уведомлений и управлять ими.</span><span class="sxs-lookup"><span data-stu-id="ea2d8-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="ea2d8-108">Командлет **Remove-AzNotificationHubsNamespace** удаляет пространство имен концентратора уведомлений из развертывания.</span><span class="sxs-lookup"><span data-stu-id="ea2d8-108">The **Remove-AzNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="ea2d8-109">При запуске этого командлета указанное пространство имен будет удалено вместе со всеми концентраторами уведомлений, связанными с этим пространством.</span><span class="sxs-lookup"><span data-stu-id="ea2d8-109">When you run this cmdlet, the specified namespace will be deleted along with all the notification hubs associated with that namespace.</span></span>

## <span data-ttu-id="ea2d8-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ea2d8-110">EXAMPLES</span></span>

### <span data-ttu-id="ea2d8-111">Пример 1: удаление пространства имен концентратора уведомлений</span><span class="sxs-lookup"><span data-stu-id="ea2d8-111">Example 1: Remove a notification hub namespace</span></span>
```
PS C:\>Remove-AzNotificationHubsNamespace -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="ea2d8-112">Эта команда удаляет пространство имен с именем ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="ea2d8-112">This command removes the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="ea2d8-113">Необходимо указать группу ресурсов, которой назначено пространство имен.</span><span class="sxs-lookup"><span data-stu-id="ea2d8-113">You must specify the resource group the namespace is assigned to.</span></span>

## <span data-ttu-id="ea2d8-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ea2d8-114">PARAMETERS</span></span>

### <span data-ttu-id="ea2d8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea2d8-115">-DefaultProfile</span></span>
<span data-ttu-id="ea2d8-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ea2d8-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ea2d8-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ea2d8-117">-Force</span></span>
<span data-ttu-id="ea2d8-118">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="ea2d8-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ea2d8-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ea2d8-119">-Namespace</span></span>
<span data-ttu-id="ea2d8-120">Задает пространство имен, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ea2d8-120">Specifies the namespace that this cmdlet removes.</span></span>
<span data-ttu-id="ea2d8-121">Пространства имен обеспечивают способ группировки и классификации концентраторов уведомлений.</span><span class="sxs-lookup"><span data-stu-id="ea2d8-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="ea2d8-122">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ea2d8-122">-ResourceGroup</span></span>
<span data-ttu-id="ea2d8-123">Указывает группу ресурсов, которой назначено пространство имен.</span><span class="sxs-lookup"><span data-stu-id="ea2d8-123">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="ea2d8-124">Группы ресурсов организуют элементы, такие как пространства имен, концентраторы уведомлений и правила авторизации, в целях простого управления запасами и администрирования Azure.</span><span class="sxs-lookup"><span data-stu-id="ea2d8-124">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="ea2d8-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ea2d8-125">-Confirm</span></span>
<span data-ttu-id="ea2d8-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ea2d8-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea2d8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea2d8-127">-WhatIf</span></span>
<span data-ttu-id="ea2d8-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ea2d8-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ea2d8-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ea2d8-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea2d8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea2d8-130">CommonParameters</span></span>
<span data-ttu-id="ea2d8-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ea2d8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea2d8-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea2d8-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea2d8-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ea2d8-133">INPUTS</span></span>

### <span data-ttu-id="ea2d8-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ea2d8-134">System.String</span></span>

## <span data-ttu-id="ea2d8-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea2d8-135">OUTPUTS</span></span>

### <span data-ttu-id="ea2d8-136">System. void</span><span class="sxs-lookup"><span data-stu-id="ea2d8-136">System.Void</span></span>

## <span data-ttu-id="ea2d8-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="ea2d8-137">NOTES</span></span>

## <span data-ttu-id="ea2d8-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ea2d8-138">RELATED LINKS</span></span>

[<span data-ttu-id="ea2d8-139">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="ea2d8-139">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="ea2d8-140">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="ea2d8-140">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="ea2d8-141">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="ea2d8-141">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


