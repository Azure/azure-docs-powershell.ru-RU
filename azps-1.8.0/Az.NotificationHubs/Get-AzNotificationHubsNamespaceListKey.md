---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F769A8AB-E025-49EE-AEA4-0D27EAEE341F
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespacelistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
ms.openlocfilehash: 88e43b182694b50169738e0b775d9202aac15ffa
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399861"
---
# <span data-ttu-id="322b3-101">Get-AzNotificationHubsNamespaceListKey</span><span class="sxs-lookup"><span data-stu-id="322b3-101">Get-AzNotificationHubsNamespaceListKey</span></span>

## <span data-ttu-id="322b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="322b3-102">SYNOPSIS</span></span>
<span data-ttu-id="322b3-103">Возвращает основные и дополнительные строки подключения, связанные с правилом авторизации пространства имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="322b3-103">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

## <span data-ttu-id="322b3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="322b3-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespaceListKey [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="322b3-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="322b3-105">DESCRIPTION</span></span>
<span data-ttu-id="322b3-106">**Cmdlet Get-AzNotificationHubsNamespaceListKey** возвращает основные и дополнительные строки подключения для правила авторизации подписи ОБЩЕГО доступа (SAS), назначенного области имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="322b3-106">The **Get-AzNotificationHubsNamespaceListKey** cmdlet returns the primary and secondary connection strings for a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>
<span data-ttu-id="322b3-107">Правила авторизации управляют правами пользователей на пространство имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="322b3-107">Authorization rules manage user rights to a notification hub namespace.</span></span>
<span data-ttu-id="322b3-108">Каждое правило содержит основную и вторичную строку подключения.</span><span class="sxs-lookup"><span data-stu-id="322b3-108">Each rule includes a primary and a secondary connection string.</span></span>

## <span data-ttu-id="322b3-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="322b3-109">EXAMPLES</span></span>

### <span data-ttu-id="322b3-110">Пример 1. Получите основные и дополнительные строки подключения для правила авторизации</span><span class="sxs-lookup"><span data-stu-id="322b3-110">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceListKey -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="322b3-111">Эта команда возвращает строки основного и дополнительного подключения для правила авторизации ListenRule, назначенного области имен ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="322b3-111">This command returns the primary and secondary connection strings for the authorization rule named ListenRule assigned to the ContosoNamespace namespace.</span></span>
<span data-ttu-id="322b3-112">При запуске этой команды необходимо включить имя группы ресурсов, которая назначена области имен.</span><span class="sxs-lookup"><span data-stu-id="322b3-112">When you run this command you must include the name of the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="322b3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="322b3-113">PARAMETERS</span></span>

### <span data-ttu-id="322b3-114">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="322b3-114">-AuthorizationRule</span></span>
<span data-ttu-id="322b3-115">Указывает имя правила проверки подлинности SAS.</span><span class="sxs-lookup"><span data-stu-id="322b3-115">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="322b3-116">Эти правила определяют тип доступа пользователей к центру уведомлений.</span><span class="sxs-lookup"><span data-stu-id="322b3-116">These rules determine the type of access that users have to the notification hub.</span></span>

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

### <span data-ttu-id="322b3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="322b3-117">-DefaultProfile</span></span>
<span data-ttu-id="322b3-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="322b3-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="322b3-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="322b3-119">-Namespace</span></span>
<span data-ttu-id="322b3-120">Определяет пространство имен, содержащее строки подключения, которые получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="322b3-120">Specifies the namespace containing the connection strings that this cmdlet gets.</span></span>

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

### <span data-ttu-id="322b3-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="322b3-121">-ResourceGroup</span></span>
<span data-ttu-id="322b3-122">Группа ресурсов, которой назначено пространство имен.</span><span class="sxs-lookup"><span data-stu-id="322b3-122">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="322b3-123">Группы ресурсов упорядочиют такие элементы, как пространства имен, концентраторы уведомлений и правила авторизации, чтобы упрость управление запасами и администрирование Azure.</span><span class="sxs-lookup"><span data-stu-id="322b3-123">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="322b3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="322b3-124">CommonParameters</span></span>
<span data-ttu-id="322b3-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="322b3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="322b3-126">Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="322b3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="322b3-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="322b3-127">INPUTS</span></span>

### <span data-ttu-id="322b3-128">System.String</span><span class="sxs-lookup"><span data-stu-id="322b3-128">System.String</span></span>

## <span data-ttu-id="322b3-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="322b3-129">OUTPUTS</span></span>

### <span data-ttu-id="322b3-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="322b3-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="322b3-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="322b3-131">NOTES</span></span>

## <span data-ttu-id="322b3-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="322b3-132">RELATED LINKS</span></span>

[<span data-ttu-id="322b3-133">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="322b3-133">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)



