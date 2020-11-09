---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 2CCDF339-9D6E-4B0C-9201-BE641C8827F6
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubpnscredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubPNSCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubPNSCredential.md
ms.openlocfilehash: 282e8092050b5859809c8dad71c4da1ee86c779d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244762"
---
# <span data-ttu-id="5bba2-101">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="5bba2-101">Get-AzNotificationHubPNSCredential</span></span>

## <span data-ttu-id="5bba2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5bba2-102">SYNOPSIS</span></span>
<span data-ttu-id="5bba2-103">Возвращает учетные данные PNS для концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="5bba2-103">Gets the PNS credentials for a notification hub.</span></span>

## <span data-ttu-id="5bba2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5bba2-104">SYNTAX</span></span>

```
Get-AzNotificationHubPNSCredential [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5bba2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5bba2-105">DESCRIPTION</span></span>
<span data-ttu-id="5bba2-106">Командлет **Get-AzNotificationHubPNSCredential** получает учетные данные службы уведомлений платформы (PNS) для концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="5bba2-106">The **Get-AzNotificationHubPNSCredential** cmdlet gets the platform notification service (PNS) credentials for a notification hub.</span></span>
<span data-ttu-id="5bba2-107">У каждого концентратора уведомлений есть один набор учетных данных PNS.</span><span class="sxs-lookup"><span data-stu-id="5bba2-107">Each notification hub has a single set of PNS credentials.</span></span>
<span data-ttu-id="5bba2-108">Эти учетные данные применяются к отдельным службам push-уведомлений, например, не ограниченным; Служба push-уведомлений iOS, Служба push-уведомлений Android и Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="5bba2-108">These credentials are applied to individual push notification services such as, but not limited to; the iOS push notification service, the Android push notification service, and Windows Phone 8.</span></span>

## <span data-ttu-id="5bba2-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5bba2-109">EXAMPLES</span></span>

### <span data-ttu-id="5bba2-110">Пример 1: получение учетных данных PNS для определенного центра уведомлений</span><span class="sxs-lookup"><span data-stu-id="5bba2-110">Example 1: Get PNS credentials for a specific notification hub</span></span>
```
PS C:\>Get-AzNotificationHubPNSCredential -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="5bba2-111">Эта команда получает учетные данные PNS для концентратора уведомлений с именем ContosoInternalHub, который принадлежит группе ресурсов с именем ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="5bba2-111">This command gets the PNS credentials for the notification hub named ContosoInternalHub that belongs to the resource group named ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="5bba2-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5bba2-112">PARAMETERS</span></span>

### <span data-ttu-id="5bba2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bba2-113">-DefaultProfile</span></span>
<span data-ttu-id="5bba2-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5bba2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5bba2-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5bba2-115">-Namespace</span></span>
<span data-ttu-id="5bba2-116">Задает пространство имен, которому назначен Центр уведомлений.</span><span class="sxs-lookup"><span data-stu-id="5bba2-116">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="5bba2-117">Пространства имен обеспечивают способ группировки и классификации концентраторов уведомлений.</span><span class="sxs-lookup"><span data-stu-id="5bba2-117">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="5bba2-118">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="5bba2-118">-NotificationHub</span></span>
<span data-ttu-id="5bba2-119">Задает центр уведомлений, которому назначаются учетные данные PNS.</span><span class="sxs-lookup"><span data-stu-id="5bba2-119">Specifies the notification hub that the PNS credentials are assigned to.</span></span>
<span data-ttu-id="5bba2-120">Концентраторы уведомлений используются для отправки push-уведомлений нескольким клиентам вне зависимости от платформы, используемой этими клиентами.</span><span class="sxs-lookup"><span data-stu-id="5bba2-120">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="5bba2-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5bba2-121">-ResourceGroup</span></span>
<span data-ttu-id="5bba2-122">Указывает группу ресурсов, которой назначен Центр уведомлений.</span><span class="sxs-lookup"><span data-stu-id="5bba2-122">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="5bba2-123">Группы ресурсов организуют элементы, такие как пространства имен, концентраторы уведомлений и правила авторизации, в целях простого управления запасами и администрирования Azure.</span><span class="sxs-lookup"><span data-stu-id="5bba2-123">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="5bba2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bba2-124">CommonParameters</span></span>
<span data-ttu-id="5bba2-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5bba2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bba2-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bba2-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bba2-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5bba2-127">INPUTS</span></span>

### <span data-ttu-id="5bba2-128">System. String</span><span class="sxs-lookup"><span data-stu-id="5bba2-128">System.String</span></span>

## <span data-ttu-id="5bba2-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5bba2-129">OUTPUTS</span></span>

### <span data-ttu-id="5bba2-130">Microsoft. Azure. Commands. NotificationHubs. Models. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="5bba2-130">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="5bba2-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="5bba2-131">NOTES</span></span>

## <span data-ttu-id="5bba2-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5bba2-132">RELATED LINKS</span></span>

[<span data-ttu-id="5bba2-133">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="5bba2-133">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

