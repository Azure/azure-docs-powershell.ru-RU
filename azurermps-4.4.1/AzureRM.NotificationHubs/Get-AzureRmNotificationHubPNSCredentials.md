---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 2CCDF339-9D6E-4B0C-9201-BE641C8827F6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubPNSCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubPNSCredentials.md
ms.openlocfilehash: 29f4871b6299685ae5791f82498083956a7e4048
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562372"
---
# <span data-ttu-id="b70f8-101">Get-AzureRmNotificationHubPNSCredentials</span><span class="sxs-lookup"><span data-stu-id="b70f8-101">Get-AzureRmNotificationHubPNSCredentials</span></span>

## <span data-ttu-id="b70f8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b70f8-102">SYNOPSIS</span></span>
<span data-ttu-id="b70f8-103">Возвращает учетные данные PNS для концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="b70f8-103">Gets the PNS credentials for a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b70f8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b70f8-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubPNSCredentials [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b70f8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b70f8-105">DESCRIPTION</span></span>
<span data-ttu-id="b70f8-106">Командлет **Get-AzureRmNotificationHubPNSCredentials** получает учетные данные службы уведомлений платформы (PNS) для концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="b70f8-106">The **Get-AzureRmNotificationHubPNSCredentials** cmdlet gets the platform notification service (PNS) credentials for a notification hub.</span></span>
<span data-ttu-id="b70f8-107">У каждого концентратора уведомлений есть один набор учетных данных PNS.</span><span class="sxs-lookup"><span data-stu-id="b70f8-107">Each notification hub has a single set of PNS credentials.</span></span>
<span data-ttu-id="b70f8-108">Эти учетные данные применяются к отдельным службам push-уведомлений, например, не ограниченным; Служба push-уведомлений iOS, Служба push-уведомлений Android и Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="b70f8-108">These credentials are applied to individual push notification services such as, but not limited to; the iOS push notification service, the Android push notification service, and Windows Phone 8.</span></span>

## <span data-ttu-id="b70f8-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b70f8-109">EXAMPLES</span></span>

### <span data-ttu-id="b70f8-110">Пример 1: получение учетных данных PNS для определенного центра уведомлений</span><span class="sxs-lookup"><span data-stu-id="b70f8-110">Example 1: Get PNS credentials for a specific notification hub</span></span>
```
PS C:\>Get-AzureRmNotificationHubPNSCredentials -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="b70f8-111">Эта команда получает учетные данные PNS для концентратора уведомлений с именем ContosoInternalHub, который принадлежит группе ресурсов с именем ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="b70f8-111">This command gets the PNS credentials for the notification hub named ContosoInternalHub that belongs to the resource group named ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="b70f8-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b70f8-112">PARAMETERS</span></span>

### <span data-ttu-id="b70f8-113">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b70f8-113">-Namespace</span></span>
<span data-ttu-id="b70f8-114">Задает пространство имен, которому назначен Центр уведомлений.</span><span class="sxs-lookup"><span data-stu-id="b70f8-114">Specifies the namespace to which the notification hub is assigned.</span></span>

<span data-ttu-id="b70f8-115">Пространства имен обеспечивают способ группировки и классификации концентраторов уведомлений.</span><span class="sxs-lookup"><span data-stu-id="b70f8-115">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="b70f8-116">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="b70f8-116">-NotificationHub</span></span>
<span data-ttu-id="b70f8-117">Задает центр уведомлений, которому назначаются учетные данные PNS.</span><span class="sxs-lookup"><span data-stu-id="b70f8-117">Specifies the notification hub that the PNS credentials are assigned to.</span></span>

<span data-ttu-id="b70f8-118">Концентраторы уведомлений используются для отправки push-уведомлений нескольким клиентам вне зависимости от платформы, используемой этими клиентами.</span><span class="sxs-lookup"><span data-stu-id="b70f8-118">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="b70f8-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b70f8-119">-ResourceGroup</span></span>
<span data-ttu-id="b70f8-120">Указывает группу ресурсов, которой назначен Центр уведомлений.</span><span class="sxs-lookup"><span data-stu-id="b70f8-120">Specifies the resource group to which the notification hub is assigned.</span></span>

<span data-ttu-id="b70f8-121">Группы ресурсов организуют элементы, такие как пространства имен, концентраторы уведомлений и правила авторизации, в целях простого управления запасами и администрирования Azure.</span><span class="sxs-lookup"><span data-stu-id="b70f8-121">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="b70f8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b70f8-122">-DefaultProfile</span></span>
<span data-ttu-id="b70f8-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b70f8-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b70f8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b70f8-124">CommonParameters</span></span>
<span data-ttu-id="b70f8-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b70f8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b70f8-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b70f8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b70f8-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b70f8-127">INPUTS</span></span>

## <span data-ttu-id="b70f8-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b70f8-128">OUTPUTS</span></span>

### <span data-ttu-id="b70f8-129">Microsoft. Azure. Commands. NotificationHubs. Models. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="b70f8-129">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="b70f8-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="b70f8-130">NOTES</span></span>

## <span data-ttu-id="b70f8-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b70f8-131">RELATED LINKS</span></span>

[<span data-ttu-id="b70f8-132">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="b70f8-132">Get-AzureRmNotificationHub</span></span>](./Get-AzureRmNotificationHub.md)


