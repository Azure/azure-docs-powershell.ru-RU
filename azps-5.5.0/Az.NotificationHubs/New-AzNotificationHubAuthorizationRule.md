---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 7E9CBEE9-DD5F-4552-9187-ECBBEF6174B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 5cfdf1eb7bfbb08d0658f4245d9e45804403135f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100236428"
---
# <span data-ttu-id="a8a36-101">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a8a36-101">New-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="a8a36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8a36-102">SYNOPSIS</span></span>
<span data-ttu-id="a8a36-103">Создает правило авторизации и назначает его центру уведомлений.</span><span class="sxs-lookup"><span data-stu-id="a8a36-103">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

## <span data-ttu-id="a8a36-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a8a36-104">SYNTAX</span></span>

### <span data-ttu-id="a8a36-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8a36-105">InputFileParameterSet</span></span>
```
New-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8a36-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8a36-106">SASRuleParameterSet</span></span>
```
New-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8a36-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8a36-107">DESCRIPTION</span></span>
<span data-ttu-id="a8a36-108">Для **создания правила авторизации new-AzNotificationHubAuthorizationRule** создается правило авторизации saS в Центре уведомлений.</span><span class="sxs-lookup"><span data-stu-id="a8a36-108">The **New-AzNotificationHubAuthorizationRule** cmdlet creates a notification hub Shared Access Signature (SAS) authorization rule.</span></span>
<span data-ttu-id="a8a36-109">Правила авторизации используются для управления доступом к концентраторам уведомлений.</span><span class="sxs-lookup"><span data-stu-id="a8a36-109">Authorization rules are used to manage access to your notification hubs.</span></span>
<span data-ttu-id="a8a36-110">Это делается путем создания ссылок ( URIS) на основе различных уровней разрешений.</span><span class="sxs-lookup"><span data-stu-id="a8a36-110">This is done by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="a8a36-111">Клиенты направляются на один из этих URL-адресов с учетом соответствующего уровня разрешений.</span><span class="sxs-lookup"><span data-stu-id="a8a36-111">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="a8a36-112">Например, клиент с разрешением на прослушивание будет направлен в URI для этого разрешения.</span><span class="sxs-lookup"><span data-stu-id="a8a36-112">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>

## <span data-ttu-id="a8a36-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a8a36-113">EXAMPLES</span></span>

### <span data-ttu-id="a8a36-114">Пример 1. Создание правила авторизации концентратора уведомлений</span><span class="sxs-lookup"><span data-stu-id="a8a36-114">Example 1: Create a notification hub authorization rule</span></span>
```
PS C:\>New-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\ExternalAccessRule.json"
```

<span data-ttu-id="a8a36-115">Эта команда создает новое правило авторизации и назначает его центру уведомлений ContosoInternalHub.</span><span class="sxs-lookup"><span data-stu-id="a8a36-115">This command creates a new authorization rule and assigns it to the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="a8a36-116">Этот центр находится в области имен ContosoNamespace и назначен группе ресурсов ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="a8a36-116">This hub is located in the ContosoNamespace namespace and is assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="a8a36-117">Обратите внимание, что все сведения о конфигурации правила, включая имя правила, будут взяты из файла ввода, C:\Configuration\ExternalAccessRule.js.</span><span class="sxs-lookup"><span data-stu-id="a8a36-117">Note that all the configuration information for the rule, including the rule name, will be taken from the input file C:\Configuration\ExternalAccessRule.json.</span></span>

## <span data-ttu-id="a8a36-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a8a36-118">PARAMETERS</span></span>

### <span data-ttu-id="a8a36-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8a36-119">-DefaultProfile</span></span>
<span data-ttu-id="a8a36-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a8a36-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a8a36-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="a8a36-121">-InputFile</span></span>
<span data-ttu-id="a8a36-122">Определяет входной файл для правила авторизации, которое создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8a36-122">Specifies the input file for the authorization rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="a8a36-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a8a36-123">-Namespace</span></span>
<span data-ttu-id="a8a36-124">Определяет пространство имен, которому назначены правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="a8a36-124">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="a8a36-125">Пространства имен предоставляют возможность группировать концентраторы уведомлений и классифицировать их.</span><span class="sxs-lookup"><span data-stu-id="a8a36-125">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="a8a36-126">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="a8a36-126">-NotificationHub</span></span>
<span data-ttu-id="a8a36-127">Указывает центр уведомлений, для который будут назначены правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="a8a36-127">Specifies the notification hub that the authorization rules will be assigned to.</span></span>
<span data-ttu-id="a8a36-128">Концентраторы уведомлений используются для отправки push-уведомлений нескольким клиентам независимо от платформы, используемой этими клиентами.</span><span class="sxs-lookup"><span data-stu-id="a8a36-128">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="a8a36-129">Обратите внимание, что необходимо указать имя существующего концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="a8a36-129">Note that you must specify the name of an existing notification hub.</span></span>
<span data-ttu-id="a8a36-130">Для создания новых концентраторов уведомлений нельзя создать новый **cmdlet New-AzNotificationHubAuthorizationRule.**</span><span class="sxs-lookup"><span data-stu-id="a8a36-130">The **New-AzNotificationHubAuthorizationRule** cmdlet cannot create new notification hubs.</span></span>

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

### <span data-ttu-id="a8a36-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a8a36-131">-ResourceGroup</span></span>
<span data-ttu-id="a8a36-132">Группа ресурсов, назначенная концентратору уведомлений.</span><span class="sxs-lookup"><span data-stu-id="a8a36-132">Specifies the resource group that the notification hub is assigned to.</span></span>

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

### <span data-ttu-id="a8a36-133">-SASRule</span><span class="sxs-lookup"><span data-stu-id="a8a36-133">-SASRule</span></span>
<span data-ttu-id="a8a36-134">Определяет объект **SharedAccessAuthorizationRuleAttributes,** содержащий сведения о конфигурации для новых правил.</span><span class="sxs-lookup"><span data-stu-id="a8a36-134">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

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

### <span data-ttu-id="a8a36-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a8a36-135">-Confirm</span></span>
<span data-ttu-id="a8a36-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8a36-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8a36-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8a36-137">-WhatIf</span></span>
<span data-ttu-id="a8a36-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8a36-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a8a36-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a8a36-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8a36-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8a36-140">CommonParameters</span></span>
<span data-ttu-id="a8a36-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8a36-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8a36-142">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8a36-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8a36-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a8a36-143">INPUTS</span></span>

### <span data-ttu-id="a8a36-144">System.String</span><span class="sxs-lookup"><span data-stu-id="a8a36-144">System.String</span></span>

## <span data-ttu-id="a8a36-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a8a36-145">OUTPUTS</span></span>

### <span data-ttu-id="a8a36-146">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="a8a36-146">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="a8a36-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a8a36-147">NOTES</span></span>

## <span data-ttu-id="a8a36-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a8a36-148">RELATED LINKS</span></span>

[<span data-ttu-id="a8a36-149">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a8a36-149">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="a8a36-150">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a8a36-150">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="a8a36-151">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a8a36-151">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


