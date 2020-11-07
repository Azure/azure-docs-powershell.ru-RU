---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 7E9CBEE9-DD5F-4552-9187-ECBBEF6174B0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/new-azurermnotificationhubauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: 8e1da1576b080f9930d123cb7ddab48761392e15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734414"
---
# <span data-ttu-id="f42be-101">New-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="f42be-101">New-AzureRmNotificationHubAuthorizationRules</span></span>

## <span data-ttu-id="f42be-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f42be-102">SYNOPSIS</span></span>
<span data-ttu-id="f42be-103">Создание правила авторизации и назначение правила для концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="f42be-103">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f42be-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f42be-104">SYNTAX</span></span>

### <span data-ttu-id="f42be-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="f42be-105">InputFileParameterSet</span></span>
```
New-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f42be-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="f42be-106">SASRuleParameterSet</span></span>
```
New-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f42be-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f42be-107">DESCRIPTION</span></span>
<span data-ttu-id="f42be-108">Командлет **New-AzureRmNotificationHubAuthorizationRules** создает правило авторизации для проверки подлинности общего доступа к подписи (SAS) центра уведомлений.</span><span class="sxs-lookup"><span data-stu-id="f42be-108">The **New-AzureRmNotificationHubAuthorizationRules** cmdlet creates a notification hub Shared Access Signature (SAS) authorization rule.</span></span>

<span data-ttu-id="f42be-109">Правила авторизации используются для управления доступом к концентраторам уведомлений.</span><span class="sxs-lookup"><span data-stu-id="f42be-109">Authorization rules are used to manage access to your notification hubs.</span></span>
<span data-ttu-id="f42be-110">Это делается путем создания ссылок в виде URI, основанных на различных уровнях разрешений.</span><span class="sxs-lookup"><span data-stu-id="f42be-110">This is done by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="f42be-111">Клиенты направляются на один из этих URI на основе соответствующего уровня разрешений.</span><span class="sxs-lookup"><span data-stu-id="f42be-111">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="f42be-112">Например, клиент, которому предоставлено разрешение прослушивания, будет направлен на универсальный код ресурса (URI) для этого разрешения.</span><span class="sxs-lookup"><span data-stu-id="f42be-112">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>

## <span data-ttu-id="f42be-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f42be-113">EXAMPLES</span></span>

### <span data-ttu-id="f42be-114">Пример 1: Создание правила авторизации на концентраторе уведомлений</span><span class="sxs-lookup"><span data-stu-id="f42be-114">Example 1: Create a notification hub authorization rule</span></span>
```
PS C:\>New-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\ExternalAccessRule.json"
```

<span data-ttu-id="f42be-115">Эта команда создает новое правило авторизации и назначает его концентратору уведомлений с именем ContosoInternalHub.</span><span class="sxs-lookup"><span data-stu-id="f42be-115">This command creates a new authorization rule and assigns it to the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="f42be-116">Этот центр расположен в пространстве имен ContosoNamespace и назначается группе ресурсов ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="f42be-116">This hub is located in the ContosoNamespace namespace and is assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="f42be-117">Обратите внимание, что все данные конфигурации для правила, включая имя правила, будут взяты из входного файла C:\Configuration\ExternalAccessRule.json.</span><span class="sxs-lookup"><span data-stu-id="f42be-117">Note that all the configuration information for the rule, including the rule name, will be taken from the input file C:\Configuration\ExternalAccessRule.json.</span></span>

## <span data-ttu-id="f42be-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f42be-118">PARAMETERS</span></span>

### <span data-ttu-id="f42be-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f42be-119">-DefaultProfile</span></span>
<span data-ttu-id="f42be-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f42be-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f42be-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="f42be-121">-InputFile</span></span>
<span data-ttu-id="f42be-122">Задает входной файл для правила авторизации, создаваемого этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="f42be-122">Specifies the input file for the authorization rule that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: InputFileParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f42be-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f42be-123">-Namespace</span></span>
<span data-ttu-id="f42be-124">Задает пространство имен, которым назначены правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="f42be-124">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="f42be-125">Пространства имен обеспечивают способ группировки и классификации концентраторов уведомлений.</span><span class="sxs-lookup"><span data-stu-id="f42be-125">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="f42be-126">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="f42be-126">-NotificationHub</span></span>
<span data-ttu-id="f42be-127">Указывает центр уведомлений, которому будут назначены правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="f42be-127">Specifies the notification hub that the authorization rules will be assigned to.</span></span>

<span data-ttu-id="f42be-128">Концентраторы уведомлений используются для отправки push-уведомлений нескольким клиентам вне зависимости от платформы, используемой этими клиентами.</span><span class="sxs-lookup"><span data-stu-id="f42be-128">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="f42be-129">Обратите внимание, что необходимо указать имя существующего концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="f42be-129">Note that you must specify the name of an existing notification hub.</span></span>
<span data-ttu-id="f42be-130">Командлет **New-AzureRmNotificationHubAuthorizationRules** не может создать новые концентраторы уведомлений.</span><span class="sxs-lookup"><span data-stu-id="f42be-130">The **New-AzureRmNotificationHubAuthorizationRules** cmdlet cannot create new notification hubs.</span></span>

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

### <span data-ttu-id="f42be-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f42be-131">-ResourceGroup</span></span>
<span data-ttu-id="f42be-132">Указывает группу ресурсов, которой назначен концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="f42be-132">Specifies the resource group that the notification hub is assigned to.</span></span>

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

### <span data-ttu-id="f42be-133">-SASRule</span><span class="sxs-lookup"><span data-stu-id="f42be-133">-SASRule</span></span>
<span data-ttu-id="f42be-134">Указывает объект **SharedAccessAuthorizationRuleAttributes** , содержащий сведения о конфигурации для новых правил.</span><span class="sxs-lookup"><span data-stu-id="f42be-134">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

```yaml
Type: SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f42be-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f42be-135">-Confirm</span></span>
<span data-ttu-id="f42be-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f42be-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f42be-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f42be-137">-WhatIf</span></span>
<span data-ttu-id="f42be-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f42be-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f42be-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f42be-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f42be-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f42be-140">CommonParameters</span></span>
<span data-ttu-id="f42be-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f42be-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f42be-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f42be-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f42be-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f42be-143">INPUTS</span></span>

### <span data-ttu-id="f42be-144">Ничего</span><span class="sxs-lookup"><span data-stu-id="f42be-144">None</span></span>
<span data-ttu-id="f42be-145">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="f42be-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f42be-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f42be-146">OUTPUTS</span></span>

### <span data-ttu-id="f42be-147">Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="f42be-147">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="f42be-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="f42be-148">NOTES</span></span>

## <span data-ttu-id="f42be-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f42be-149">RELATED LINKS</span></span>

[<span data-ttu-id="f42be-150">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="f42be-150">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="f42be-151">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="f42be-151">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="f42be-152">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="f42be-152">Set-AzureRmNotificationHubAuthorizationRules</span></span>](./Set-AzureRmNotificationHubAuthorizationRules.md)


