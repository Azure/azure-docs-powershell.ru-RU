---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: F769A8AB-E025-49EE-AEA4-0D27EAEE341F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhubsnamespacelistkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceListKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceListKeys.md
ms.openlocfilehash: 2fb9eeb3b5d6bcc3a2183bc652b74caa370e4d02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564707"
---
# <span data-ttu-id="6e6b4-101">Get-AzureRmNotificationHubsNamespaceListKeys</span><span class="sxs-lookup"><span data-stu-id="6e6b4-101">Get-AzureRmNotificationHubsNamespaceListKeys</span></span>

## <span data-ttu-id="6e6b4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6e6b4-102">SYNOPSIS</span></span>
<span data-ttu-id="6e6b4-103">Получает первичные и вторичные строки подключения, связанные с правилом авторизации пространства имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="6e6b4-103">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e6b4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6e6b4-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubsNamespaceListKeys [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e6b4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e6b4-105">DESCRIPTION</span></span>
<span data-ttu-id="6e6b4-106">Командлет **Get-AzureRmNotificationHubsNamespaceListKeys** Возвращает основную и вспомогательную строки подключения для правила авторизации, назначенного пространству имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="6e6b4-106">The **Get-AzureRmNotificationHubsNamespaceListKeys** cmdlet returns the primary and secondary connection strings for a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>

<span data-ttu-id="6e6b4-107">Правила авторизации управляют правами пользователей на пространство имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="6e6b4-107">Authorization rules manage user rights to a notification hub namespace.</span></span>
<span data-ttu-id="6e6b4-108">Каждое правило включает в себя первичную и вспомогательную строку подключения.</span><span class="sxs-lookup"><span data-stu-id="6e6b4-108">Each rule includes a primary and a secondary connection string.</span></span>

## <span data-ttu-id="6e6b4-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6e6b4-109">EXAMPLES</span></span>

### <span data-ttu-id="6e6b4-110">Пример 1: получение первичных и дополнительных строк подключения для правила авторизации</span><span class="sxs-lookup"><span data-stu-id="6e6b4-110">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespaceListKeys -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="6e6b4-111">Эта команда возвращает первичные и дополнительные строки подключения для правила авторизации с именем ListenRule, назначенного пространству имен ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="6e6b4-111">This command returns the primary and secondary connection strings for the authorization rule named ListenRule assigned to the ContosoNamespace namespace.</span></span>
<span data-ttu-id="6e6b4-112">При выполнении этой команды необходимо включить имя группы ресурсов, которой назначено пространство имен.</span><span class="sxs-lookup"><span data-stu-id="6e6b4-112">When you run this command you must include the name of the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="6e6b4-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6e6b4-113">PARAMETERS</span></span>

### <span data-ttu-id="6e6b4-114">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6e6b4-114">-AuthorizationRule</span></span>
<span data-ttu-id="6e6b4-115">Указывает имя правила проверки подлинности SAS.</span><span class="sxs-lookup"><span data-stu-id="6e6b4-115">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="6e6b4-116">Эти правила определяют тип доступа пользователей к концентратору уведомлений.</span><span class="sxs-lookup"><span data-stu-id="6e6b4-116">These rules determine the type of access that users have to the notification hub.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e6b4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e6b4-117">-DefaultProfile</span></span>
<span data-ttu-id="6e6b4-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6e6b4-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6e6b4-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6e6b4-119">-Namespace</span></span>
<span data-ttu-id="6e6b4-120">Задает пространство имен, содержащее строки подключения, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="6e6b4-120">Specifies the namespace containing the connection strings that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6e6b4-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6e6b4-121">-ResourceGroup</span></span>
<span data-ttu-id="6e6b4-122">Указывает группу ресурсов, которой назначено пространство имен.</span><span class="sxs-lookup"><span data-stu-id="6e6b4-122">Specifies the resource group to which the namespace is assigned.</span></span>

<span data-ttu-id="6e6b4-123">Группы ресурсов организуют элементы, такие как пространства имен, концентраторы уведомлений и правила авторизации, в целях простого управления запасами и администрирования Azure.</span><span class="sxs-lookup"><span data-stu-id="6e6b4-123">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="6e6b4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e6b4-124">CommonParameters</span></span>
<span data-ttu-id="6e6b4-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6e6b4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e6b4-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e6b4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e6b4-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6e6b4-127">INPUTS</span></span>

### <span data-ttu-id="6e6b4-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="6e6b4-128">None</span></span>
<span data-ttu-id="6e6b4-129">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="6e6b4-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6e6b4-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e6b4-130">OUTPUTS</span></span>

### <span data-ttu-id="6e6b4-131">Microsoft. Azure. Management. NotificationHubs. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="6e6b4-131">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="6e6b4-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="6e6b4-132">NOTES</span></span>

## <span data-ttu-id="6e6b4-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6e6b4-133">RELATED LINKS</span></span>

[<span data-ttu-id="6e6b4-134">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="6e6b4-134">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="6e6b4-135">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="6e6b4-135">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)


