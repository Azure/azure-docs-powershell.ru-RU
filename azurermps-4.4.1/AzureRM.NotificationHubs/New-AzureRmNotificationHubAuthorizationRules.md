---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 7E9CBEE9-DD5F-4552-9187-ECBBEF6174B0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: c3a30457e6fd25aa633a0faa0510ed4ce61efbd0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565218"
---
# <span data-ttu-id="0a1fd-101">New-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="0a1fd-101">New-AzureRmNotificationHubAuthorizationRules</span></span>

## <span data-ttu-id="0a1fd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0a1fd-102">SYNOPSIS</span></span>
<span data-ttu-id="0a1fd-103">Создание правила авторизации и назначение правила для концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="0a1fd-103">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a1fd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0a1fd-104">SYNTAX</span></span>

### <span data-ttu-id="0a1fd-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a1fd-105">InputFileParameterSet</span></span>
```
New-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a1fd-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a1fd-106">SASRuleParameterSet</span></span>
```
New-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a1fd-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a1fd-107">DESCRIPTION</span></span>
<span data-ttu-id="0a1fd-108">Командлет **New-AzureRmNotificationHubAuthorizationRules** создает правило авторизации для проверки подлинности общего доступа к подписи (SAS) центра уведомлений.</span><span class="sxs-lookup"><span data-stu-id="0a1fd-108">The **New-AzureRmNotificationHubAuthorizationRules** cmdlet creates a notification hub Shared Access Signature (SAS) authorization rule.</span></span>

<span data-ttu-id="0a1fd-109">Правила авторизации используются для управления доступом к концентраторам уведомлений.</span><span class="sxs-lookup"><span data-stu-id="0a1fd-109">Authorization rules are used to manage access to your notification hubs.</span></span>
<span data-ttu-id="0a1fd-110">Это делается путем создания ссылок в виде URI, основанных на различных уровнях разрешений.</span><span class="sxs-lookup"><span data-stu-id="0a1fd-110">This is done by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="0a1fd-111">Клиенты направляются на один из этих URI на основе соответствующего уровня разрешений.</span><span class="sxs-lookup"><span data-stu-id="0a1fd-111">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="0a1fd-112">Например, клиент, которому предоставлено разрешение прослушивания, будет направлен на универсальный код ресурса (URI) для этого разрешения.</span><span class="sxs-lookup"><span data-stu-id="0a1fd-112">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>

## <span data-ttu-id="0a1fd-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0a1fd-113">EXAMPLES</span></span>

### <span data-ttu-id="0a1fd-114">Пример 1: Создание правила авторизации на концентраторе уведомлений</span><span class="sxs-lookup"><span data-stu-id="0a1fd-114">Example 1: Create a notification hub authorization rule</span></span>
```
PS C:\>New-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\ExternalAccessRule.json"
```

<span data-ttu-id="0a1fd-115">Эта команда создает новое правило авторизации и назначает его концентратору уведомлений с именем ContosoInternalHub.</span><span class="sxs-lookup"><span data-stu-id="0a1fd-115">This command creates a new authorization rule and assigns it to the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="0a1fd-116">Этот центр расположен в пространстве имен ContosoNamespace и назначается группе ресурсов ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="0a1fd-116">This hub is located in the ContosoNamespace namespace and is assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="0a1fd-117">Обратите внимание, что все данные конфигурации для правила, включая имя правила, будут взяты из входного файла C:\Configuration\ExternalAccessRule.json.</span><span class="sxs-lookup"><span data-stu-id="0a1fd-117">Note that all the configuration information for the rule, including the rule name, will be taken from the input file C:\Configuration\ExternalAccessRule.json.</span></span>

## <span data-ttu-id="0a1fd-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0a1fd-118">PARAMETERS</span></span>

### <span data-ttu-id="0a1fd-119">-InputFile</span><span class="sxs-lookup"><span data-stu-id="0a1fd-119">-InputFile</span></span>
<span data-ttu-id="0a1fd-120">Задает входной файл для правила авторизации, создаваемого этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="0a1fd-120">Specifies the input file for the authorization rule that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a1fd-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0a1fd-121">-Namespace</span></span>
<span data-ttu-id="0a1fd-122">Задает пространство имен, которым назначены правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="0a1fd-122">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="0a1fd-123">Пространства имен обеспечивают способ группировки и классификации концентраторов уведомлений.</span><span class="sxs-lookup"><span data-stu-id="0a1fd-123">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="0a1fd-124">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="0a1fd-124">-NotificationHub</span></span>
<span data-ttu-id="0a1fd-125">Указывает центр уведомлений, которому будут назначены правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="0a1fd-125">Specifies the notification hub that the authorization rules will be assigned to.</span></span>

<span data-ttu-id="0a1fd-126">Концентраторы уведомлений используются для отправки push-уведомлений нескольким клиентам вне зависимости от платформы, используемой этими клиентами.</span><span class="sxs-lookup"><span data-stu-id="0a1fd-126">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="0a1fd-127">Обратите внимание, что необходимо указать имя существующего концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="0a1fd-127">Note that you must specify the name of an existing notification hub.</span></span>
<span data-ttu-id="0a1fd-128">Командлет **New-AzureRmNotificationHubAuthorizationRules** не может создать новые концентраторы уведомлений.</span><span class="sxs-lookup"><span data-stu-id="0a1fd-128">The **New-AzureRmNotificationHubAuthorizationRules** cmdlet cannot create new notification hubs.</span></span>

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

### <span data-ttu-id="0a1fd-129">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0a1fd-129">-ResourceGroup</span></span>
<span data-ttu-id="0a1fd-130">Указывает группу ресурсов, которой назначен концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="0a1fd-130">Specifies the resource group that the notification hub is assigned to.</span></span>

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

### <span data-ttu-id="0a1fd-131">-SASRule</span><span class="sxs-lookup"><span data-stu-id="0a1fd-131">-SASRule</span></span>
<span data-ttu-id="0a1fd-132">Указывает объект **SharedAccessAuthorizationRuleAttributes** , содержащий сведения о конфигурации для новых правил.</span><span class="sxs-lookup"><span data-stu-id="0a1fd-132">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a1fd-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0a1fd-133">-Confirm</span></span>
<span data-ttu-id="0a1fd-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0a1fd-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a1fd-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a1fd-135">-WhatIf</span></span>
<span data-ttu-id="0a1fd-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0a1fd-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0a1fd-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0a1fd-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a1fd-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a1fd-138">-DefaultProfile</span></span>
<span data-ttu-id="0a1fd-139">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0a1fd-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a1fd-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a1fd-140">CommonParameters</span></span>
<span data-ttu-id="0a1fd-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0a1fd-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a1fd-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a1fd-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a1fd-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0a1fd-143">INPUTS</span></span>

## <span data-ttu-id="0a1fd-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a1fd-144">OUTPUTS</span></span>

### <span data-ttu-id="0a1fd-145">Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="0a1fd-145">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="0a1fd-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="0a1fd-146">NOTES</span></span>

## <span data-ttu-id="0a1fd-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0a1fd-147">RELATED LINKS</span></span>

[<span data-ttu-id="0a1fd-148">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="0a1fd-148">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="0a1fd-149">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="0a1fd-149">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="0a1fd-150">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="0a1fd-150">Set-AzureRmNotificationHubAuthorizationRules</span></span>](./Set-AzureRmNotificationHubAuthorizationRules.md)


