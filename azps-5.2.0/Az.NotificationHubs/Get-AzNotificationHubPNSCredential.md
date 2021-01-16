---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 2CCDF339-9D6E-4B0C-9201-BE641C8827F6
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubpnscredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubPNSCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubPNSCredential.md
ms.openlocfilehash: 282e8092050b5859809c8dad71c4da1ee86c779d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404919"
---
# <span data-ttu-id="13314-101">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="13314-101">Get-AzNotificationHubPNSCredential</span></span>

## <span data-ttu-id="13314-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13314-102">SYNOPSIS</span></span>
<span data-ttu-id="13314-103">Получает учетные данные PNS для концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="13314-103">Gets the PNS credentials for a notification hub.</span></span>

## <span data-ttu-id="13314-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="13314-104">SYNTAX</span></span>

```
Get-AzNotificationHubPNSCredential [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13314-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="13314-105">DESCRIPTION</span></span>
<span data-ttu-id="13314-106">**Cmdlet Get-AzNotificationHubPNSCredential** получает учетные данные службы уведомлений платформы (PNS) для концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="13314-106">The **Get-AzNotificationHubPNSCredential** cmdlet gets the platform notification service (PNS) credentials for a notification hub.</span></span>
<span data-ttu-id="13314-107">Каждый концентратор уведомлений имеет один набор учетных данных PNS.</span><span class="sxs-lookup"><span data-stu-id="13314-107">Each notification hub has a single set of PNS credentials.</span></span>
<span data-ttu-id="13314-108">Эти учетные данные применяются к отдельным службам push-уведомлений, таким как: служба push-уведомлений iOS, служба push-уведомлений Android и Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="13314-108">These credentials are applied to individual push notification services such as, but not limited to; the iOS push notification service, the Android push notification service, and Windows Phone 8.</span></span>

## <span data-ttu-id="13314-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="13314-109">EXAMPLES</span></span>

### <span data-ttu-id="13314-110">Пример 1. Получить учетные данные PNS для определенного концентратора уведомлений</span><span class="sxs-lookup"><span data-stu-id="13314-110">Example 1: Get PNS credentials for a specific notification hub</span></span>
```
PS C:\>Get-AzNotificationHubPNSCredential -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="13314-111">Эта команда получает учетные данные PNS для концентратора уведомлений ContosoInternalHub, который принадлежит к группе ресурсов ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="13314-111">This command gets the PNS credentials for the notification hub named ContosoInternalHub that belongs to the resource group named ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="13314-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13314-112">PARAMETERS</span></span>

### <span data-ttu-id="13314-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13314-113">-DefaultProfile</span></span>
<span data-ttu-id="13314-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="13314-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="13314-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="13314-115">-Namespace</span></span>
<span data-ttu-id="13314-116">Определяет пространство имен, которому назначен концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="13314-116">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="13314-117">Пространства имен предоставляют возможность группировать и классифицировать концентраторы уведомлений.</span><span class="sxs-lookup"><span data-stu-id="13314-117">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="13314-118">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="13314-118">-NotificationHub</span></span>
<span data-ttu-id="13314-119">Указывает центр уведомлений, для который назначены учетные данные PNS.</span><span class="sxs-lookup"><span data-stu-id="13314-119">Specifies the notification hub that the PNS credentials are assigned to.</span></span>
<span data-ttu-id="13314-120">Концентраторы уведомлений используются для отправки push-уведомлений нескольким клиентам независимо от платформы, используемой этими клиентами.</span><span class="sxs-lookup"><span data-stu-id="13314-120">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="13314-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="13314-121">-ResourceGroup</span></span>
<span data-ttu-id="13314-122">Группа ресурсов, которой назначен концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="13314-122">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="13314-123">Группы ресурсов упорядочиют такие элементы, как пространства имен, концентраторы уведомлений и правила авторизации, чтобы упрость управление запасами и администрирование Azure.</span><span class="sxs-lookup"><span data-stu-id="13314-123">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="13314-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13314-124">CommonParameters</span></span>
<span data-ttu-id="13314-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13314-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13314-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13314-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13314-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="13314-127">INPUTS</span></span>

### <span data-ttu-id="13314-128">System.String</span><span class="sxs-lookup"><span data-stu-id="13314-128">System.String</span></span>

## <span data-ttu-id="13314-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="13314-129">OUTPUTS</span></span>

### <span data-ttu-id="13314-130">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="13314-130">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="13314-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="13314-131">NOTES</span></span>

## <span data-ttu-id="13314-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="13314-132">RELATED LINKS</span></span>

[<span data-ttu-id="13314-133">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="13314-133">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)


