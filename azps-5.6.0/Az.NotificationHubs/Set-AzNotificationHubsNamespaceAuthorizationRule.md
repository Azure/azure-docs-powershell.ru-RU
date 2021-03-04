---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F0981A7A-1B17-4141-A267-927E5B78BE5F
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/set-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: 2f5ff44e6d96900afe36b9ade8360fb0a69ec726
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951096"
---
# <span data-ttu-id="80c9b-101">Set-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="80c9b-101">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="80c9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80c9b-102">SYNOPSIS</span></span>
<span data-ttu-id="80c9b-103">Задает правила авторизации для пространства имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="80c9b-103">Sets authorization rules for a notification hub namespace.</span></span>

## <span data-ttu-id="80c9b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="80c9b-104">SYNTAX</span></span>

### <span data-ttu-id="80c9b-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="80c9b-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="80c9b-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="80c9b-106">SASRuleParameterSet</span></span>
```
Set-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80c9b-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="80c9b-107">DESCRIPTION</span></span>
<span data-ttu-id="80c9b-108">**Cmdlet Set-AzNotificationHubsNamespaceAuthorizationRule** изменяет правило авторизации подписи общего доступа (SAS), назначенное области имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="80c9b-108">The **Set-AzNotificationHubsNamespaceAuthorizationRule** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>
<span data-ttu-id="80c9b-109">Правила авторизации управляют правами пользователей на пространство имен и на концентраторы уведомлений, содержащиеся в этом пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="80c9b-109">Authorization rules manage user rights to the namespace and to the notification hubs contained in that namespace.</span></span>
<span data-ttu-id="80c9b-110">Этот cmdlet предоставляет два способа изменения правила авторизации, назначенного для пространства имен.</span><span class="sxs-lookup"><span data-stu-id="80c9b-110">This cmdlet provides two ways to modify an authorization rule assigned to a namespace.</span></span>
<span data-ttu-id="80c9b-111">Например, вы можете создать экземпляр объекта **SharedAccessAuthorizationRuleAttributes,** а затем настроить его со значениями свойств, которые должны подавляться правилу.</span><span class="sxs-lookup"><span data-stu-id="80c9b-111">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="80c9b-112">Для этого можно использовать платформа .NET Framework вехи.</span><span class="sxs-lookup"><span data-stu-id="80c9b-112">You can use the .NET Framework to accomplish this.</span></span>
<span data-ttu-id="80c9b-113">Затем вы можете скопировать значения этих свойств в правило с помощью параметра *SASRule.*</span><span class="sxs-lookup"><span data-stu-id="80c9b-113">You can then copy those property values to the rule through the *SASRule* parameter.</span></span>
<span data-ttu-id="80c9b-114">Кроме того, можно создать файл нотации объектов JSON (JavaScript), содержащий соответствующие значения конфигурации, и применить их с помощью параметра *InputFile.*</span><span class="sxs-lookup"><span data-stu-id="80c9b-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="80c9b-115">JSON-файл — это текстовый файл с синтаксисом, аналогичным {</span><span class="sxs-lookup"><span data-stu-id="80c9b-115">A JSON file is a text file that uses syntax similar to this: {</span></span>  
    <span data-ttu-id="80c9b-116">"Name": "ContosoAuthorizationRule",</span><span class="sxs-lookup"><span data-stu-id="80c9b-116">"Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="80c9b-117">"PrimaryKey": "WE4qH0398AyXj извещенt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span><span class="sxs-lookup"><span data-stu-id="80c9b-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="80c9b-118">"Права": \[</span><span class="sxs-lookup"><span data-stu-id="80c9b-118">"Rights": \[</span></span>  
        <span data-ttu-id="80c9b-119">"Прослушивание",</span><span class="sxs-lookup"><span data-stu-id="80c9b-119">"Listen",</span></span>  
        <span data-ttu-id="80c9b-120">"Отправить"</span><span class="sxs-lookup"><span data-stu-id="80c9b-120">"Send"</span></span>  
    \]  
<span data-ttu-id="80c9b-121">} При использовании в сочетании с cmdlet **Set-AzNotificationHubsNamespaceAuthorizationRule** в предыдущем примере JSON изменяет правило авторизации с именем ContosoAuthorizationRule, чтобы предоставить пользователям права на прослушивание и отправку прав на пространство имен.</span><span class="sxs-lookup"><span data-stu-id="80c9b-121">} When used in conjunction with the **Set-AzNotificationHubsNamespaceAuthorizationRule** cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule to give users Listen and Send rights to the namespace.</span></span>

## <span data-ttu-id="80c9b-122">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="80c9b-122">EXAMPLES</span></span>

### <span data-ttu-id="80c9b-123">Пример 1. Изменение правила авторизации, назначенного для пространства имен</span><span class="sxs-lookup"><span data-stu-id="80c9b-123">Example 1: Modify an authorization rule assigned to a namespace</span></span>
```
PS C:\>Set-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="80c9b-124">Эта команда изменяет правило авторизации, назначенное области имен с именем ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="80c9b-124">This command modifies an authorization rule assigned to the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="80c9b-125">Необходимо указать группу ресурсов, которая назначена области имен.</span><span class="sxs-lookup"><span data-stu-id="80c9b-125">You must specify the resource group that the namespace is assigned to.</span></span>
<span data-ttu-id="80c9b-126">Сведения о правиле авторизации не включаются в команду.</span><span class="sxs-lookup"><span data-stu-id="80c9b-126">Information about the authorization rule is not included in the command itself.</span></span>
<span data-ttu-id="80c9b-127">Эта информация будет получена из входного файла, C:\Configuration\AuthorizationRules.jsвходной файл.</span><span class="sxs-lookup"><span data-stu-id="80c9b-127">Instead, that information is obtained from the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="80c9b-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80c9b-128">PARAMETERS</span></span>

### <span data-ttu-id="80c9b-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80c9b-129">-DefaultProfile</span></span>
<span data-ttu-id="80c9b-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="80c9b-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="80c9b-131">-Force</span><span class="sxs-lookup"><span data-stu-id="80c9b-131">-Force</span></span>
<span data-ttu-id="80c9b-132">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="80c9b-132">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="80c9b-133">-InputFile</span><span class="sxs-lookup"><span data-stu-id="80c9b-133">-InputFile</span></span>
<span data-ttu-id="80c9b-134">Путь к файлу JSON, содержащего сведения о конфигурации для нового правила.</span><span class="sxs-lookup"><span data-stu-id="80c9b-134">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80c9b-135">-Namespace</span><span class="sxs-lookup"><span data-stu-id="80c9b-135">-Namespace</span></span>
<span data-ttu-id="80c9b-136">Определяет пространство имен, которое содержит правила авторизации, которые изменяет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80c9b-136">Specifies the namespace that contains the authorization rules that this cmdlet modifies.</span></span>
<span data-ttu-id="80c9b-137">Пространства имен предоставляют возможность группировать концентраторы уведомлений и классифицировать их.</span><span class="sxs-lookup"><span data-stu-id="80c9b-137">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="80c9b-138">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="80c9b-138">-ResourceGroup</span></span>
<span data-ttu-id="80c9b-139">Группа ресурсов, которой назначено пространство имен.</span><span class="sxs-lookup"><span data-stu-id="80c9b-139">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="80c9b-140">Группы ресурсов упорядочиют такие элементы, как пространства имен, концентраторы уведомлений и правила авторизации, чтобы упрость управление запасами и администрирование Azure.</span><span class="sxs-lookup"><span data-stu-id="80c9b-140">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="80c9b-141">-SASRule</span><span class="sxs-lookup"><span data-stu-id="80c9b-141">-SASRule</span></span>
<span data-ttu-id="80c9b-142">Указывает объект **SharedAccessAuthorizationRuleAttributes,** который содержит сведения о конфигурации для правил авторизации, которые изменяет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80c9b-142">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that this cmdlet modifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80c9b-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="80c9b-143">-Confirm</span></span>
<span data-ttu-id="80c9b-144">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="80c9b-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80c9b-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80c9b-145">-WhatIf</span></span>
<span data-ttu-id="80c9b-146">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80c9b-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="80c9b-147">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="80c9b-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80c9b-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80c9b-148">CommonParameters</span></span>
<span data-ttu-id="80c9b-149">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80c9b-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80c9b-150">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80c9b-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80c9b-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="80c9b-151">INPUTS</span></span>

### <span data-ttu-id="80c9b-152">System.String</span><span class="sxs-lookup"><span data-stu-id="80c9b-152">System.String</span></span>

## <span data-ttu-id="80c9b-153">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="80c9b-153">OUTPUTS</span></span>

### <span data-ttu-id="80c9b-154">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="80c9b-154">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="80c9b-155">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="80c9b-155">NOTES</span></span>

## <span data-ttu-id="80c9b-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="80c9b-156">RELATED LINKS</span></span>

[<span data-ttu-id="80c9b-157">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="80c9b-157">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="80c9b-158">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="80c9b-158">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./New-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="80c9b-159">Remove-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="80c9b-159">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Remove-AzNotificationHubsNamespaceAuthorizationRule.md)


