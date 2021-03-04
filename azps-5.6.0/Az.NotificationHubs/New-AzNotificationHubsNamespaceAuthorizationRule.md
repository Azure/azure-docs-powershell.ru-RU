---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3F59F7E8-CD32-40CB-9DE0-3FB044439DD0
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/new-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: 49a856ef38d529c7d60b7c09b4d4a4fcdab5b59b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951251"
---
# <span data-ttu-id="82cdc-101">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="82cdc-101">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="82cdc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82cdc-102">SYNOPSIS</span></span>
<span data-ttu-id="82cdc-103">Создает правило авторизации и назначает его области имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="82cdc-103">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

## <span data-ttu-id="82cdc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="82cdc-104">SYNTAX</span></span>

### <span data-ttu-id="82cdc-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="82cdc-105">InputFileParameterSet</span></span>
```
New-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82cdc-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="82cdc-106">SASRuleParameterSet</span></span>
```
New-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82cdc-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="82cdc-107">DESCRIPTION</span></span>
<span data-ttu-id="82cdc-108">Для создания правила авторизации saS создается правило авторизации SAS с новыми **именамиHubsNamespaceAuthorizationRule** и назначается пространство имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="82cdc-108">The **New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet creates a Shared Access Signature (SAS) authorization rule and assigns it to a notification hub namespace.</span></span>
<span data-ttu-id="82cdc-109">Правила авторизации управляют правами пользователей на пространство имен и в концентраторы уведомлений, содержащиеся в этом пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="82cdc-109">Authorization rules manage user rights to the namespace and to the notification hubs contained with that namespace.</span></span>
<span data-ttu-id="82cdc-110">Этот cmdlet предоставляет два способа создать новое правило авторизации и назначить его в область имен.</span><span class="sxs-lookup"><span data-stu-id="82cdc-110">This cmdlet provides two ways to create a new authorization rule and assign it to a namespace.</span></span>
<span data-ttu-id="82cdc-111">Вы можете создать экземпляр объекта **SharedAccessAuthorizationRuleAttributes,** а затем настроить его со значениями свойств, которые должны притяжаться новым правилом.</span><span class="sxs-lookup"><span data-stu-id="82cdc-111">You can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the new rule to possess.</span></span>
<span data-ttu-id="82cdc-112">Это можно сделать с помощью платформа .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="82cdc-112">This can be done using .NET Framework.</span></span>
<span data-ttu-id="82cdc-113">Затем вы можете скопировать значения этих свойств в новое правило с помощью *параметра SASRule.*</span><span class="sxs-lookup"><span data-stu-id="82cdc-113">You can then copy those property values to your new rule by using *SASRule* parameter.</span></span>
<span data-ttu-id="82cdc-114">Кроме того, можно создать файл нотации объектов JSON (JavaScript), содержащий соответствующие значения конфигурации, а затем применить их с помощью параметра *InputFile.*</span><span class="sxs-lookup"><span data-stu-id="82cdc-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values by using the *InputFile* parameter.</span></span>
<span data-ttu-id="82cdc-115">JSON-файл — это текстовый файл с синтаксисом, аналогичным следующему: {</span><span class="sxs-lookup"><span data-stu-id="82cdc-115">A JSON file is a text file that uses syntax similar to the following: {</span></span>  
    <span data-ttu-id="82cdc-116">"Name": "ContosoAuthorizationRule",</span><span class="sxs-lookup"><span data-stu-id="82cdc-116">"Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="82cdc-117">"PrimaryKey": "WE4qH0398AyXj извещенt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span><span class="sxs-lookup"><span data-stu-id="82cdc-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="82cdc-118">"Права": \[</span><span class="sxs-lookup"><span data-stu-id="82cdc-118">"Rights": \[</span></span>  
        <span data-ttu-id="82cdc-119">"Прослушивание",</span><span class="sxs-lookup"><span data-stu-id="82cdc-119">"Listen",</span></span>  
        <span data-ttu-id="82cdc-120">"Отправить"</span><span class="sxs-lookup"><span data-stu-id="82cdc-120">"Send"</span></span>  
    \]  
<span data-ttu-id="82cdc-121">} При использовании в сочетании с cmdlet **New-AzNotificationHubsNamespaceAuthorizationRule** в предыдущем примере JSON создается правило авторизации с именем ContosoAuthorizationRule, которое позволяет пользователям прослушать и отправить права на пространство имен.</span><span class="sxs-lookup"><span data-stu-id="82cdc-121">} When used in conjunction with the **New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet, the preceding JSON sample creates an authorization rule named ContosoAuthorizationRule that gives users Listen and Send rights to the namespace.</span></span>
<span data-ttu-id="82cdc-122">*Первичныйkey,* используемый для проверки подлинности, может быть случайным образом создан с помощью следующей команды Windows PowerShell: \[ Convert \] ::ToBase64String((1,32 |% { \[ byte/](Get-Random -Minimum 0 -Maximum 255) }))</span><span class="sxs-lookup"><span data-stu-id="82cdc-122">The *PrimaryKey* that is used for authentication, can be randomly generated by using the following Windows PowerShell command: \[Convert\]::ToBase64String((1..32 |% { \[byte/](Get-Random -Minimum 0 -Maximum 255) }))</span></span>

## <span data-ttu-id="82cdc-123">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="82cdc-123">EXAMPLES</span></span>

### <span data-ttu-id="82cdc-124">Пример 1. Создание правила авторизации и назначение его области имен</span><span class="sxs-lookup"><span data-stu-id="82cdc-124">Example 1: Create an authorization rule and assign it to a namespace</span></span>
```
PS C:\>New-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\NamespaceAuthorizationRules.json"
```

<span data-ttu-id="82cdc-125">Эта команда создает правило авторизации и назначает его области имен ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="82cdc-125">This command creates an authorization rule and assigns that rule to the namespace ContosoNamespace.</span></span>
<span data-ttu-id="82cdc-126">При создании этого правила необходимо указать соответствующее пространство имен и группу ресурсов, которая назначена этому пространству.</span><span class="sxs-lookup"><span data-stu-id="82cdc-126">When creating this rule you must specify the appropriate namespace and the resource group that the namespace is assigned to.</span></span>
<span data-ttu-id="82cdc-127">Однако указывать какие-либо сведения о правиле не требуется: сведения о правиле будут взяты из файла ввода, C:\Configuration\NamespaceAuthorizationRules.js.</span><span class="sxs-lookup"><span data-stu-id="82cdc-127">However, you do not need to specify any information about the rule itself: rule information will be taken from the input file C:\Configuration\NamespaceAuthorizationRules.json.</span></span>

## <span data-ttu-id="82cdc-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82cdc-128">PARAMETERS</span></span>

### <span data-ttu-id="82cdc-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82cdc-129">-DefaultProfile</span></span>
<span data-ttu-id="82cdc-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="82cdc-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="82cdc-131">-InputFile</span><span class="sxs-lookup"><span data-stu-id="82cdc-131">-InputFile</span></span>
<span data-ttu-id="82cdc-132">Путь к файлу JSON, содержащего сведения о конфигурации для нового правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="82cdc-132">Specifies the path to a JSON file containing configuration information for the new authorization rule.</span></span>

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

### <span data-ttu-id="82cdc-133">-Namespace</span><span class="sxs-lookup"><span data-stu-id="82cdc-133">-Namespace</span></span>
<span data-ttu-id="82cdc-134">Определяет пространство имен, в которое будут назначены правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="82cdc-134">Specifies the namespace to which the authorization rules will be assigned.</span></span>
<span data-ttu-id="82cdc-135">Пространства имен предоставляют возможность группировать и классифицировать концентраторы уведомлений.</span><span class="sxs-lookup"><span data-stu-id="82cdc-135">Namespaces provide a way to group and categorize notification hubs.</span></span>
<span data-ttu-id="82cdc-136">Новые правила должны быть назначены существующему пространству имен.</span><span class="sxs-lookup"><span data-stu-id="82cdc-136">The new rules must be assigned to an existing namespace.</span></span>
<span data-ttu-id="82cdc-137">Для **создания нового пространства имен нельзя** создать новое пространство имен.</span><span class="sxs-lookup"><span data-stu-id="82cdc-137">The **New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet cannot create a new namespace.</span></span>

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

### <span data-ttu-id="82cdc-138">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="82cdc-138">-ResourceGroup</span></span>
<span data-ttu-id="82cdc-139">Группа ресурсов, которой назначено пространство имен.</span><span class="sxs-lookup"><span data-stu-id="82cdc-139">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="82cdc-140">Группы ресурсов упорядочиют такие элементы, как пространства имен, концентраторы уведомлений и правила авторизации, чтобы упрость управление запасами и администрирование Azure.</span><span class="sxs-lookup"><span data-stu-id="82cdc-140">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>
<span data-ttu-id="82cdc-141">Необходимо использовать существующую группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="82cdc-141">You must use an existing resource group.</span></span>
<span data-ttu-id="82cdc-142">Этот cmdlet не может создать новую группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="82cdc-142">This cmdlet cannot create a new resource group.</span></span>

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

### <span data-ttu-id="82cdc-143">-SASRule</span><span class="sxs-lookup"><span data-stu-id="82cdc-143">-SASRule</span></span>
<span data-ttu-id="82cdc-144">Определяет объект **SharedAccessAuthorizationRuleAttributes,** содержащий сведения о конфигурации для новых правил.</span><span class="sxs-lookup"><span data-stu-id="82cdc-144">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

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

### <span data-ttu-id="82cdc-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82cdc-145">-Confirm</span></span>
<span data-ttu-id="82cdc-146">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82cdc-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82cdc-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82cdc-147">-WhatIf</span></span>
<span data-ttu-id="82cdc-148">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82cdc-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="82cdc-149">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="82cdc-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82cdc-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82cdc-150">CommonParameters</span></span>
<span data-ttu-id="82cdc-151">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82cdc-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82cdc-152">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82cdc-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82cdc-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="82cdc-153">INPUTS</span></span>

### <span data-ttu-id="82cdc-154">System.String</span><span class="sxs-lookup"><span data-stu-id="82cdc-154">System.String</span></span>

## <span data-ttu-id="82cdc-155">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="82cdc-155">OUTPUTS</span></span>

### <span data-ttu-id="82cdc-156">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="82cdc-156">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="82cdc-157">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="82cdc-157">NOTES</span></span>

## <span data-ttu-id="82cdc-158">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="82cdc-158">RELATED LINKS</span></span>

[<span data-ttu-id="82cdc-159">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="82cdc-159">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="82cdc-160">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="82cdc-160">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="82cdc-161">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="82cdc-161">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


