---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F769A8AB-E025-49EE-AEA4-0D27EAEE341F
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespacelistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
ms.openlocfilehash: 2217a0c8aa68e815b650cd3eb564ce7a21733e72
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246053"
---
# <span data-ttu-id="c43ae-101">Get-AzNotificationHubsNamespaceListKey</span><span class="sxs-lookup"><span data-stu-id="c43ae-101">Get-AzNotificationHubsNamespaceListKey</span></span>

## <span data-ttu-id="c43ae-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c43ae-102">SYNOPSIS</span></span>
<span data-ttu-id="c43ae-103">Получает первичные и вторичные строки подключения, связанные с правилом авторизации пространства имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="c43ae-103">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

## <span data-ttu-id="c43ae-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c43ae-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespaceListKey [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c43ae-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c43ae-105">DESCRIPTION</span></span>
<span data-ttu-id="c43ae-106">Командлет **Get-AzNotificationHubsNamespaceListKey** Возвращает основную и вспомогательную строки подключения для правила авторизации, назначенного пространству имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="c43ae-106">The **Get-AzNotificationHubsNamespaceListKey** cmdlet returns the primary and secondary connection strings for a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>
<span data-ttu-id="c43ae-107">Правила авторизации управляют правами пользователей на пространство имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="c43ae-107">Authorization rules manage user rights to a notification hub namespace.</span></span>
<span data-ttu-id="c43ae-108">Каждое правило включает в себя первичную и вспомогательную строку подключения.</span><span class="sxs-lookup"><span data-stu-id="c43ae-108">Each rule includes a primary and a secondary connection string.</span></span>

## <span data-ttu-id="c43ae-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c43ae-109">EXAMPLES</span></span>

### <span data-ttu-id="c43ae-110">Пример 1: получение первичных и дополнительных строк подключения для правила авторизации</span><span class="sxs-lookup"><span data-stu-id="c43ae-110">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceListKey -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="c43ae-111">Эта команда возвращает первичные и дополнительные строки подключения для правила авторизации с именем ListenRule, назначенного пространству имен ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="c43ae-111">This command returns the primary and secondary connection strings for the authorization rule named ListenRule assigned to the ContosoNamespace namespace.</span></span>
<span data-ttu-id="c43ae-112">При выполнении этой команды необходимо включить имя группы ресурсов, которой назначено пространство имен.</span><span class="sxs-lookup"><span data-stu-id="c43ae-112">When you run this command you must include the name of the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="c43ae-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c43ae-113">PARAMETERS</span></span>

### <span data-ttu-id="c43ae-114">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c43ae-114">-AuthorizationRule</span></span>
<span data-ttu-id="c43ae-115">Указывает имя правила проверки подлинности SAS.</span><span class="sxs-lookup"><span data-stu-id="c43ae-115">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="c43ae-116">Эти правила определяют тип доступа пользователей к концентратору уведомлений.</span><span class="sxs-lookup"><span data-stu-id="c43ae-116">These rules determine the type of access that users have to the notification hub.</span></span>

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

### <span data-ttu-id="c43ae-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c43ae-117">-DefaultProfile</span></span>
<span data-ttu-id="c43ae-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c43ae-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c43ae-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c43ae-119">-Namespace</span></span>
<span data-ttu-id="c43ae-120">Задает пространство имен, содержащее строки подключения, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c43ae-120">Specifies the namespace containing the connection strings that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c43ae-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c43ae-121">-ResourceGroup</span></span>
<span data-ttu-id="c43ae-122">Указывает группу ресурсов, которой назначено пространство имен.</span><span class="sxs-lookup"><span data-stu-id="c43ae-122">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="c43ae-123">Группы ресурсов организуют элементы, такие как пространства имен, концентраторы уведомлений и правила авторизации, в целях простого управления запасами и администрирования Azure.</span><span class="sxs-lookup"><span data-stu-id="c43ae-123">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="c43ae-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c43ae-124">CommonParameters</span></span>
<span data-ttu-id="c43ae-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c43ae-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c43ae-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c43ae-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c43ae-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c43ae-127">INPUTS</span></span>

### <span data-ttu-id="c43ae-128">System. String</span><span class="sxs-lookup"><span data-stu-id="c43ae-128">System.String</span></span>

## <span data-ttu-id="c43ae-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c43ae-129">OUTPUTS</span></span>

### <span data-ttu-id="c43ae-130">Microsoft. Azure. Management. NotificationHubs. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="c43ae-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="c43ae-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="c43ae-131">NOTES</span></span>

## <span data-ttu-id="c43ae-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c43ae-132">RELATED LINKS</span></span>

[<span data-ttu-id="c43ae-133">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="c43ae-133">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="c43ae-134">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c43ae-134">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)


