---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 5EDFBF19-928F-4F95-BD93-CF8BAEA11C52
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/remove-azurermnotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: 2a728cdae95c117e73f38b16cdea5407c1f4954e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561659"
---
# <span data-ttu-id="47a45-101">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="47a45-101">Remove-AzureRmNotificationHubsNamespace</span></span>

## <span data-ttu-id="47a45-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="47a45-102">SYNOPSIS</span></span>
<span data-ttu-id="47a45-103">Удаляет пространство имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="47a45-103">Removes a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47a45-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="47a45-104">SYNTAX</span></span>

```
Remove-AzureRmNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47a45-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="47a45-105">DESCRIPTION</span></span>
<span data-ttu-id="47a45-106">Командлет **Remove-AzureRmNotificationHubsNamespace** удаляет пространство имен концентратора уведомлений из развертывания.</span><span class="sxs-lookup"><span data-stu-id="47a45-106">The **Remove-AzureRmNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>

<span data-ttu-id="47a45-107">Пространства имен — это логические контейнеры, помогающие упорядочивать концентраторы уведомлений и управлять ими.</span><span class="sxs-lookup"><span data-stu-id="47a45-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="47a45-108">Командлет **Remove-AzureRmNotificationHubsNamespace** удаляет пространство имен концентратора уведомлений из развертывания.</span><span class="sxs-lookup"><span data-stu-id="47a45-108">The **Remove-AzureRmNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="47a45-109">При запуске этого командлета указанное пространство имен будет удалено вместе со всеми концентраторами уведомлений, связанными с этим пространством.</span><span class="sxs-lookup"><span data-stu-id="47a45-109">When you run this cmdlet, the specified namespace will be deleted along with all the notification hubs associated with that namespace.</span></span>

## <span data-ttu-id="47a45-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="47a45-110">EXAMPLES</span></span>

### <span data-ttu-id="47a45-111">Пример 1: удаление пространства имен концентратора уведомлений</span><span class="sxs-lookup"><span data-stu-id="47a45-111">Example 1: Remove a notification hub namespace</span></span>
```
PS C:\>Remove-AzureRmNotificationHubsNamespace -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="47a45-112">Эта команда удаляет пространство имен с именем ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="47a45-112">This command removes the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="47a45-113">Необходимо указать группу ресурсов, которой назначено пространство имен.</span><span class="sxs-lookup"><span data-stu-id="47a45-113">You must specify the resource group the namespace is assigned to.</span></span>

## <span data-ttu-id="47a45-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="47a45-114">PARAMETERS</span></span>

### <span data-ttu-id="47a45-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47a45-115">-DefaultProfile</span></span>
<span data-ttu-id="47a45-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="47a45-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="47a45-117">-Force</span><span class="sxs-lookup"><span data-stu-id="47a45-117">-Force</span></span>
<span data-ttu-id="47a45-118">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="47a45-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="47a45-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="47a45-119">-Namespace</span></span>
<span data-ttu-id="47a45-120">Задает пространство имен, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="47a45-120">Specifies the namespace that this cmdlet removes.</span></span>
<span data-ttu-id="47a45-121">Пространства имен обеспечивают способ группировки и классификации концентраторов уведомлений.</span><span class="sxs-lookup"><span data-stu-id="47a45-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="47a45-122">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="47a45-122">-ResourceGroup</span></span>
<span data-ttu-id="47a45-123">Указывает группу ресурсов, которой назначено пространство имен.</span><span class="sxs-lookup"><span data-stu-id="47a45-123">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="47a45-124">Группы ресурсов организуют элементы, такие как пространства имен, концентраторы уведомлений и правила авторизации, в целях простого управления запасами и администрирования Azure.</span><span class="sxs-lookup"><span data-stu-id="47a45-124">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="47a45-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="47a45-125">-Confirm</span></span>
<span data-ttu-id="47a45-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="47a45-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47a45-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47a45-127">-WhatIf</span></span>
<span data-ttu-id="47a45-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="47a45-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="47a45-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="47a45-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47a45-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47a45-130">CommonParameters</span></span>
<span data-ttu-id="47a45-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="47a45-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47a45-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47a45-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47a45-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="47a45-133">INPUTS</span></span>

### <span data-ttu-id="47a45-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="47a45-134">None</span></span>
<span data-ttu-id="47a45-135">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="47a45-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="47a45-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="47a45-136">OUTPUTS</span></span>

## <span data-ttu-id="47a45-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="47a45-137">NOTES</span></span>

## <span data-ttu-id="47a45-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="47a45-138">RELATED LINKS</span></span>

[<span data-ttu-id="47a45-139">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="47a45-139">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="47a45-140">New-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="47a45-140">New-AzureRmNotificationHubsNamespace</span></span>](./New-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="47a45-141">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="47a45-141">Set-AzureRmNotificationHubsNamespace</span></span>](./Set-AzureRmNotificationHubsNamespace.md)


