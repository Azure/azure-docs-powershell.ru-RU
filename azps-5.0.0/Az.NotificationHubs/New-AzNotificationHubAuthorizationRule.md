---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 7E9CBEE9-DD5F-4552-9187-ECBBEF6174B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 5cfdf1eb7bfbb08d0658f4245d9e45804403135f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245937"
---
# <span data-ttu-id="5c022-101">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5c022-101">New-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="5c022-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5c022-102">SYNOPSIS</span></span>
<span data-ttu-id="5c022-103">Создание правила авторизации и назначение правила для концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="5c022-103">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

## <span data-ttu-id="5c022-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5c022-104">SYNTAX</span></span>

### <span data-ttu-id="5c022-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c022-105">InputFileParameterSet</span></span>
```
New-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c022-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c022-106">SASRuleParameterSet</span></span>
```
New-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c022-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c022-107">DESCRIPTION</span></span>
<span data-ttu-id="5c022-108">Командлет **New-AzNotificationHubAuthorizationRule** создает правило авторизации для проверки подлинности общего доступа к подписи (SAS) центра уведомлений.</span><span class="sxs-lookup"><span data-stu-id="5c022-108">The **New-AzNotificationHubAuthorizationRule** cmdlet creates a notification hub Shared Access Signature (SAS) authorization rule.</span></span>
<span data-ttu-id="5c022-109">Правила авторизации используются для управления доступом к концентраторам уведомлений.</span><span class="sxs-lookup"><span data-stu-id="5c022-109">Authorization rules are used to manage access to your notification hubs.</span></span>
<span data-ttu-id="5c022-110">Это делается путем создания ссылок в виде URI, основанных на различных уровнях разрешений.</span><span class="sxs-lookup"><span data-stu-id="5c022-110">This is done by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="5c022-111">Клиенты направляются на один из этих URI на основе соответствующего уровня разрешений.</span><span class="sxs-lookup"><span data-stu-id="5c022-111">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="5c022-112">Например, клиент, которому предоставлено разрешение прослушивания, будет направлен на универсальный код ресурса (URI) для этого разрешения.</span><span class="sxs-lookup"><span data-stu-id="5c022-112">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>

## <span data-ttu-id="5c022-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5c022-113">EXAMPLES</span></span>

### <span data-ttu-id="5c022-114">Пример 1: Создание правила авторизации на концентраторе уведомлений</span><span class="sxs-lookup"><span data-stu-id="5c022-114">Example 1: Create a notification hub authorization rule</span></span>
```
PS C:\>New-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\ExternalAccessRule.json"
```

<span data-ttu-id="5c022-115">Эта команда создает новое правило авторизации и назначает его концентратору уведомлений с именем ContosoInternalHub.</span><span class="sxs-lookup"><span data-stu-id="5c022-115">This command creates a new authorization rule and assigns it to the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="5c022-116">Этот центр расположен в пространстве имен ContosoNamespace и назначается группе ресурсов ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="5c022-116">This hub is located in the ContosoNamespace namespace and is assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="5c022-117">Обратите внимание, что все данные конфигурации для правила, включая имя правила, будут взяты из входного файла C:\Configuration\ExternalAccessRule.json.</span><span class="sxs-lookup"><span data-stu-id="5c022-117">Note that all the configuration information for the rule, including the rule name, will be taken from the input file C:\Configuration\ExternalAccessRule.json.</span></span>

## <span data-ttu-id="5c022-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5c022-118">PARAMETERS</span></span>

### <span data-ttu-id="5c022-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c022-119">-DefaultProfile</span></span>
<span data-ttu-id="5c022-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5c022-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5c022-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="5c022-121">-InputFile</span></span>
<span data-ttu-id="5c022-122">Задает входной файл для правила авторизации, создаваемого этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="5c022-122">Specifies the input file for the authorization rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="5c022-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5c022-123">-Namespace</span></span>
<span data-ttu-id="5c022-124">Задает пространство имен, которым назначены правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="5c022-124">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="5c022-125">Пространства имен обеспечивают способ группировки и классификации концентраторов уведомлений.</span><span class="sxs-lookup"><span data-stu-id="5c022-125">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="5c022-126">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="5c022-126">-NotificationHub</span></span>
<span data-ttu-id="5c022-127">Указывает центр уведомлений, которому будут назначены правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="5c022-127">Specifies the notification hub that the authorization rules will be assigned to.</span></span>
<span data-ttu-id="5c022-128">Концентраторы уведомлений используются для отправки push-уведомлений нескольким клиентам вне зависимости от платформы, используемой этими клиентами.</span><span class="sxs-lookup"><span data-stu-id="5c022-128">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="5c022-129">Обратите внимание, что необходимо указать имя существующего концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="5c022-129">Note that you must specify the name of an existing notification hub.</span></span>
<span data-ttu-id="5c022-130">Командлет **New-AzNotificationHubAuthorizationRule** не может создать новые концентраторы уведомлений.</span><span class="sxs-lookup"><span data-stu-id="5c022-130">The **New-AzNotificationHubAuthorizationRule** cmdlet cannot create new notification hubs.</span></span>

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

### <span data-ttu-id="5c022-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5c022-131">-ResourceGroup</span></span>
<span data-ttu-id="5c022-132">Указывает группу ресурсов, которой назначен концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="5c022-132">Specifies the resource group that the notification hub is assigned to.</span></span>

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

### <span data-ttu-id="5c022-133">-SASRule</span><span class="sxs-lookup"><span data-stu-id="5c022-133">-SASRule</span></span>
<span data-ttu-id="5c022-134">Указывает объект **SharedAccessAuthorizationRuleAttributes** , содержащий сведения о конфигурации для новых правил.</span><span class="sxs-lookup"><span data-stu-id="5c022-134">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

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

### <span data-ttu-id="5c022-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5c022-135">-Confirm</span></span>
<span data-ttu-id="5c022-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5c022-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c022-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c022-137">-WhatIf</span></span>
<span data-ttu-id="5c022-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5c022-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5c022-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5c022-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c022-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c022-140">CommonParameters</span></span>
<span data-ttu-id="5c022-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5c022-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c022-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c022-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c022-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5c022-143">INPUTS</span></span>

### <span data-ttu-id="5c022-144">System. String</span><span class="sxs-lookup"><span data-stu-id="5c022-144">System.String</span></span>

## <span data-ttu-id="5c022-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c022-145">OUTPUTS</span></span>

### <span data-ttu-id="5c022-146">Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="5c022-146">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="5c022-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="5c022-147">NOTES</span></span>

## <span data-ttu-id="5c022-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5c022-148">RELATED LINKS</span></span>

[<span data-ttu-id="5c022-149">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5c022-149">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="5c022-150">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5c022-150">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="5c022-151">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5c022-151">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


