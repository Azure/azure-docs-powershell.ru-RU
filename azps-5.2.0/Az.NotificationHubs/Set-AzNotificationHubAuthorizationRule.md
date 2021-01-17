---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: BD311CEF-378B-463E-8998-CC3E9A5B3A7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: f95b016380f640154533f69d3942b8fe12a064d7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395204"
---
# <span data-ttu-id="085d7-101">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="085d7-101">Set-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="085d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="085d7-102">SYNOPSIS</span></span>
<span data-ttu-id="085d7-103">Задает правила авторизации для концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="085d7-103">Sets authorization rules for a notification hub.</span></span>

## <span data-ttu-id="085d7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="085d7-104">SYNTAX</span></span>

### <span data-ttu-id="085d7-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="085d7-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="085d7-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="085d7-106">SASRuleParameterSet</span></span>
```
Set-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="085d7-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="085d7-107">DESCRIPTION</span></span>
<span data-ttu-id="085d7-108">**CmdletRule Set-AzNotificationHubAuthorizationRule** изменяет правило авторизации подписи общего доступа (SAS), назначенное центру уведомлений.</span><span class="sxs-lookup"><span data-stu-id="085d7-108">The **Set-AzNotificationHubAuthorizationRule** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub.</span></span>
<span data-ttu-id="085d7-109">Правила авторизации управляют доступом к концентраторам уведомлений путем создания ссылок в качестве URIS на основе различных уровней разрешений.</span><span class="sxs-lookup"><span data-stu-id="085d7-109">Authorization rules manage access to your notification hubs by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="085d7-110">Уровни разрешений могут быть следующими:</span><span class="sxs-lookup"><span data-stu-id="085d7-110">Permission levels can be one of the following:</span></span> 
- <span data-ttu-id="085d7-111">Прослушивание</span><span class="sxs-lookup"><span data-stu-id="085d7-111">Listen</span></span>
- <span data-ttu-id="085d7-112">Отправить</span><span class="sxs-lookup"><span data-stu-id="085d7-112">Send</span></span>
- <span data-ttu-id="085d7-113">Управление клиентами направляется на один из этих ЮРИСов с учетом соответствующего уровня разрешений.</span><span class="sxs-lookup"><span data-stu-id="085d7-113">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="085d7-114">Например, клиент с разрешением на прослушивание будет направлен в URI для этого разрешения.</span><span class="sxs-lookup"><span data-stu-id="085d7-114">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="085d7-115">Этот cmdlet предоставляет два способа изменения правила авторизации, назначенного центру уведомлений.</span><span class="sxs-lookup"><span data-stu-id="085d7-115">This cmdlet provides two ways to modify an authorization rule assigned to a notification hub.</span></span>
<span data-ttu-id="085d7-116">Например, вы можете создать экземпляр объекта **SharedAccessAuthorizationRuleAttributes,** а затем настроить для него значения свойств, которые должны притяжаться правилом.</span><span class="sxs-lookup"><span data-stu-id="085d7-116">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="085d7-117">Объект можно настроить с помощью .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="085d7-117">You can configure the object through the .NET Framework.</span></span>
<span data-ttu-id="085d7-118">Затем вы можете скопировать значения этих свойств в правило с помощью *параметра SASRule.*</span><span class="sxs-lookup"><span data-stu-id="085d7-118">You can then copy those property values to your rule by using *SASRule* parameter.</span></span>
<span data-ttu-id="085d7-119">Кроме того, можно создать файл нотации объектов JSON (JavaScript), содержащий соответствующие значения конфигурации, и применить их с помощью параметра *InputFile.*</span><span class="sxs-lookup"><span data-stu-id="085d7-119">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="085d7-120">JSON-файл — это текстовый файл с синтаксисом примерно такого синтаксиса: { "Name": "ContosoAuthorizationRule",</span><span class="sxs-lookup"><span data-stu-id="085d7-120">A JSON file is a text file that uses syntax similar to this: {      "Name": "ContosoAuthorizationRule",</span></span>  
  <span data-ttu-id="085d7-121">"PrimaryKey": "WE4qH0398AyXj извещенt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span><span class="sxs-lookup"><span data-stu-id="085d7-121">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
  <span data-ttu-id="085d7-122">"Права": \[</span><span class="sxs-lookup"><span data-stu-id="085d7-122">"Rights": \[</span></span>  
        <span data-ttu-id="085d7-123">"Прослушивание",</span><span class="sxs-lookup"><span data-stu-id="085d7-123">"Listen",</span></span>  
        <span data-ttu-id="085d7-124">"Отправить"</span><span class="sxs-lookup"><span data-stu-id="085d7-124">"Send"</span></span>  
    \]  
  <span data-ttu-id="085d7-125">} При использовании в сочетании с New-AzNotificationHubAuthorizationRule в предыдущем примере JSON изменяется правило авторизации с именем ContosoAuthorizationRule, чтобы предоставить пользователям права на прослушивание и отправку прав на концентратор.</span><span class="sxs-lookup"><span data-stu-id="085d7-125">} When used in conjunction with the New-AzNotificationHubAuthorizationRule cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule in order to give users Listen and Send rights to the hub.</span></span>

## <span data-ttu-id="085d7-126">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="085d7-126">EXAMPLES</span></span>

### <span data-ttu-id="085d7-127">Пример 1. Изменение правила авторизации, назначенного центру уведомлений</span><span class="sxs-lookup"><span data-stu-id="085d7-127">Example 1: Modify an authorization rule assigned to a notification hub</span></span>
```
PS C:\>Set-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -NotificationHub "ContosoExternalHub" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="085d7-128">Эта команда изменяет правило авторизации, назначенное центру уведомлений ContosoExternalHub.</span><span class="sxs-lookup"><span data-stu-id="085d7-128">This command modifies an authorization rule assigned to the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="085d7-129">Необходимо указать пространство имен, в котором находится центр, а также группу ресурсов, которой он назначен.</span><span class="sxs-lookup"><span data-stu-id="085d7-129">You must specify the namespace where the hub is located as well as the resource group that the hub is assigned.</span></span>
<span data-ttu-id="085d7-130">Сведения о измененном правиле не включаются в самую команду.</span><span class="sxs-lookup"><span data-stu-id="085d7-130">Information about the rule that is modified is not included in the command itself.</span></span>
<span data-ttu-id="085d7-131">Эти сведения можно найти во входных файлах, C:\Configuration\AuthorizationRules.jsвходных данных.</span><span class="sxs-lookup"><span data-stu-id="085d7-131">Instead, that information is found in the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="085d7-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="085d7-132">PARAMETERS</span></span>

### <span data-ttu-id="085d7-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="085d7-133">-DefaultProfile</span></span>
<span data-ttu-id="085d7-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="085d7-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="085d7-135">-Force</span><span class="sxs-lookup"><span data-stu-id="085d7-135">-Force</span></span>
<span data-ttu-id="085d7-136">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="085d7-136">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="085d7-137">-InputFile</span><span class="sxs-lookup"><span data-stu-id="085d7-137">-InputFile</span></span>
<span data-ttu-id="085d7-138">Путь к файлу JSON, содержащего сведения о конфигурации для нового правила.</span><span class="sxs-lookup"><span data-stu-id="085d7-138">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

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

### <span data-ttu-id="085d7-139">-Namespace</span><span class="sxs-lookup"><span data-stu-id="085d7-139">-Namespace</span></span>
<span data-ttu-id="085d7-140">Определяет пространство имен, которому назначен концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="085d7-140">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="085d7-141">Пространства имен предоставляют возможность группировать концентраторы уведомлений и классифицировать их.</span><span class="sxs-lookup"><span data-stu-id="085d7-141">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="085d7-142">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="085d7-142">-NotificationHub</span></span>
<span data-ttu-id="085d7-143">Указывает центр уведомлений, для который этот cmdlet назначает правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="085d7-143">Specifies the notification hub that this cmdlet assigns authorization rules to.</span></span>
<span data-ttu-id="085d7-144">Концентраторы уведомлений используются для отправки push-уведомлений нескольким клиентам независимо от их использования.</span><span class="sxs-lookup"><span data-stu-id="085d7-144">Notification hubs are used to send push notifications to multiple clients regardless of the used by those clients.</span></span>

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

### <span data-ttu-id="085d7-145">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="085d7-145">-ResourceGroup</span></span>
<span data-ttu-id="085d7-146">Группа ресурсов, которой назначен концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="085d7-146">Specifies the resource group to which the notification hub is assigned.</span></span> <span data-ttu-id="085d7-147">Группы ресурсов упорядочиют такие элементы, как пространства имен, концентраторы уведомлений и правила авторизации, чтобы упрость управление запасами и администрирование Azure.</span><span class="sxs-lookup"><span data-stu-id="085d7-147">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="085d7-148">-SASRule</span><span class="sxs-lookup"><span data-stu-id="085d7-148">-SASRule</span></span>
<span data-ttu-id="085d7-149">Указывает объект **SharedAccessAuthorizationRuleAttributes,** содержащий сведения о конфигурации для измененных правил авторизации.</span><span class="sxs-lookup"><span data-stu-id="085d7-149">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that are modified.</span></span>

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

### <span data-ttu-id="085d7-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="085d7-150">-Confirm</span></span>
<span data-ttu-id="085d7-151">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="085d7-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="085d7-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="085d7-152">-WhatIf</span></span>
<span data-ttu-id="085d7-153">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="085d7-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="085d7-154">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="085d7-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="085d7-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="085d7-155">CommonParameters</span></span>
<span data-ttu-id="085d7-156">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="085d7-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="085d7-157">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="085d7-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="085d7-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="085d7-158">INPUTS</span></span>

### <span data-ttu-id="085d7-159">System.String</span><span class="sxs-lookup"><span data-stu-id="085d7-159">System.String</span></span>

## <span data-ttu-id="085d7-160">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="085d7-160">OUTPUTS</span></span>

### <span data-ttu-id="085d7-161">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="085d7-161">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="085d7-162">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="085d7-162">NOTES</span></span>

## <span data-ttu-id="085d7-163">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="085d7-163">RELATED LINKS</span></span>

[<span data-ttu-id="085d7-164">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="085d7-164">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="085d7-165">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="085d7-165">New-AzNotificationHubAuthorizationRule</span></span>](./New-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="085d7-166">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="085d7-166">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)


