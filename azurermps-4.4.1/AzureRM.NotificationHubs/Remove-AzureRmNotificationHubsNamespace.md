---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 5EDFBF19-928F-4F95-BD93-CF8BAEA11C52
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: ff315c7f3634c0a8a4afd5c4b54926c0a260ed75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562348"
---
# <span data-ttu-id="2b8fc-101">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="2b8fc-101">Remove-AzureRmNotificationHubsNamespace</span></span>

## <span data-ttu-id="2b8fc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2b8fc-102">SYNOPSIS</span></span>
<span data-ttu-id="2b8fc-103">Удаляет пространство имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="2b8fc-103">Removes a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b8fc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2b8fc-104">SYNTAX</span></span>

```
Remove-AzureRmNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b8fc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b8fc-105">DESCRIPTION</span></span>
<span data-ttu-id="2b8fc-106">Командлет **Remove-AzureRmNotificationHubsNamespace** удаляет пространство имен концентратора уведомлений из развертывания.</span><span class="sxs-lookup"><span data-stu-id="2b8fc-106">The **Remove-AzureRmNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>

<span data-ttu-id="2b8fc-107">Пространства имен — это логические контейнеры, помогающие упорядочивать концентраторы уведомлений и управлять ими.</span><span class="sxs-lookup"><span data-stu-id="2b8fc-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="2b8fc-108">Командлет **Remove-AzureRmNotificationHubsNamespace** удаляет пространство имен концентратора уведомлений из развертывания.</span><span class="sxs-lookup"><span data-stu-id="2b8fc-108">The **Remove-AzureRmNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="2b8fc-109">При запуске этого командлета указанное пространство имен будет удалено вместе со всеми концентраторами уведомлений, связанными с этим пространством.</span><span class="sxs-lookup"><span data-stu-id="2b8fc-109">When you run this cmdlet, the specified namespace will be deleted along with all the notification hubs associated with that namespace.</span></span>

## <span data-ttu-id="2b8fc-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2b8fc-110">EXAMPLES</span></span>

### <span data-ttu-id="2b8fc-111">Пример 1: удаление пространства имен концентратора уведомлений</span><span class="sxs-lookup"><span data-stu-id="2b8fc-111">Example 1: Remove a notification hub namespace</span></span>
```
PS C:\>Remove-AzureRmNotificationHubsNamespace -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="2b8fc-112">Эта команда удаляет пространство имен с именем ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="2b8fc-112">This command removes the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="2b8fc-113">Необходимо указать группу ресурсов, которой назначено пространство имен.</span><span class="sxs-lookup"><span data-stu-id="2b8fc-113">You must specify the resource group the namespace is assigned to.</span></span>

## <span data-ttu-id="2b8fc-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2b8fc-114">PARAMETERS</span></span>

### <span data-ttu-id="2b8fc-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2b8fc-115">-Force</span></span>
<span data-ttu-id="2b8fc-116">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="2b8fc-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2b8fc-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2b8fc-117">-Namespace</span></span>
<span data-ttu-id="2b8fc-118">Задает пространство имен, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="2b8fc-118">Specifies the namespace that this cmdlet removes.</span></span>
<span data-ttu-id="2b8fc-119">Пространства имен обеспечивают способ группировки и классификации концентраторов уведомлений.</span><span class="sxs-lookup"><span data-stu-id="2b8fc-119">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="2b8fc-120">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2b8fc-120">-ResourceGroup</span></span>
<span data-ttu-id="2b8fc-121">Указывает группу ресурсов, которой назначено пространство имен.</span><span class="sxs-lookup"><span data-stu-id="2b8fc-121">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="2b8fc-122">Группы ресурсов организуют элементы, такие как пространства имен, концентраторы уведомлений и правила авторизации, в целях простого управления запасами и администрирования Azure.</span><span class="sxs-lookup"><span data-stu-id="2b8fc-122">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="2b8fc-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2b8fc-123">-Confirm</span></span>
<span data-ttu-id="2b8fc-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2b8fc-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b8fc-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b8fc-125">-WhatIf</span></span>
<span data-ttu-id="2b8fc-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2b8fc-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2b8fc-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2b8fc-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b8fc-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b8fc-128">-DefaultProfile</span></span>
<span data-ttu-id="2b8fc-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2b8fc-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b8fc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b8fc-130">CommonParameters</span></span>
<span data-ttu-id="2b8fc-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2b8fc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b8fc-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b8fc-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b8fc-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2b8fc-133">INPUTS</span></span>

## <span data-ttu-id="2b8fc-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b8fc-134">OUTPUTS</span></span>

## <span data-ttu-id="2b8fc-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="2b8fc-135">NOTES</span></span>

## <span data-ttu-id="2b8fc-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2b8fc-136">RELATED LINKS</span></span>

[<span data-ttu-id="2b8fc-137">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="2b8fc-137">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="2b8fc-138">New-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="2b8fc-138">New-AzureRmNotificationHubsNamespace</span></span>](./New-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="2b8fc-139">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="2b8fc-139">Set-AzureRmNotificationHubsNamespace</span></span>](./Set-AzureRmNotificationHubsNamespace.md)


