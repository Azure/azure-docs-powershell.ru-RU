---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: F0981A7A-1B17-4141-A267-927E5B78BE5F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/set-azurermnotificationhubsnamespaceauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: f86eff8bae46e2a9f626566ccfdcc6e3d23a6e82
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732591"
---
# <span data-ttu-id="bd2a0-101">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="bd2a0-101">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>

## <span data-ttu-id="bd2a0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bd2a0-102">SYNOPSIS</span></span>
<span data-ttu-id="bd2a0-103">Задает правила авторизации для пространства имен центра уведомлений.</span><span class="sxs-lookup"><span data-stu-id="bd2a0-103">Sets authorization rules for a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd2a0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bd2a0-104">SYNTAX</span></span>

### <span data-ttu-id="bd2a0-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd2a0-105">InputFileParameterSet</span></span>
```
Set-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bd2a0-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd2a0-106">SASRuleParameterSet</span></span>
```
Set-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd2a0-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd2a0-107">DESCRIPTION</span></span>
<span data-ttu-id="bd2a0-108">Командлет **Set-AzureRmNotificationHubsNamespaceAuthorizationRules** изменяет правило авторизации подписи общего доступа (SAS), назначенное пространству имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="bd2a0-108">The **Set-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>
<span data-ttu-id="bd2a0-109">Правила авторизации управляют правами пользователей на пространство имен и на концентраторы уведомлений, содержащиеся в этом пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="bd2a0-109">Authorization rules manage user rights to the namespace and to the notification hubs contained in that namespace.</span></span>
<span data-ttu-id="bd2a0-110">Этот командлет предоставляет два способа изменения правила авторизации, назначенного пространству имен.</span><span class="sxs-lookup"><span data-stu-id="bd2a0-110">This cmdlet provides two ways to modify an authorization rule assigned to a namespace.</span></span>
<span data-ttu-id="bd2a0-111">Для одного из них вы можете создать экземпляр объекта **SharedAccessAuthorizationRuleAttributes** , а затем настроить этот объект с помощью значений свойств, которым должно обладать правило.</span><span class="sxs-lookup"><span data-stu-id="bd2a0-111">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="bd2a0-112">Для этого можно использовать платформу .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="bd2a0-112">You can use the .NET Framework to accomplish this.</span></span>
<span data-ttu-id="bd2a0-113">Затем значения этих свойств можно скопировать в правило с помощью параметра *SASRule* .</span><span class="sxs-lookup"><span data-stu-id="bd2a0-113">You can then copy those property values to the rule through the *SASRule* parameter.</span></span>
<span data-ttu-id="bd2a0-114">Кроме того, вы можете создать файл JSON (объектной нотации JavaScript), содержащий соответствующие значения конфигурации, и применить эти значения с помощью параметра *inputFile* .</span><span class="sxs-lookup"><span data-stu-id="bd2a0-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="bd2a0-115">JSON-файл — это текстовый файл, в котором используются такие же синтаксисы: {</span><span class="sxs-lookup"><span data-stu-id="bd2a0-115">A JSON file is a text file that uses syntax similar to this: {</span></span>  
    <span data-ttu-id="bd2a0-116">"Имя": "ContosoAuthorizationRule";</span><span class="sxs-lookup"><span data-stu-id="bd2a0-116">"Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="bd2a0-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =";</span><span class="sxs-lookup"><span data-stu-id="bd2a0-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="bd2a0-118">"Права": \[</span><span class="sxs-lookup"><span data-stu-id="bd2a0-118">"Rights": \[</span></span>  
        <span data-ttu-id="bd2a0-119">"Прослушать",</span><span class="sxs-lookup"><span data-stu-id="bd2a0-119">"Listen",</span></span>  
        <span data-ttu-id="bd2a0-120">Отправить</span><span class="sxs-lookup"><span data-stu-id="bd2a0-120">"Send"</span></span>  
    \]  
<span data-ttu-id="bd2a0-121">} При использовании в сочетании с командлетом **Set-AzureRmNotificationHubsNamespaceAuthorizationRules** предыдущий пример JSON изменяет правило авторизации с именем ContosoAuthorizationRule, чтобы дать пользователям возможность прослушивать и отправлять права на пространство имен.</span><span class="sxs-lookup"><span data-stu-id="bd2a0-121">} When used in conjunction with the **Set-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule to give users Listen and Send rights to the namespace.</span></span>

## <span data-ttu-id="bd2a0-122">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bd2a0-122">EXAMPLES</span></span>

### <span data-ttu-id="bd2a0-123">Пример 1: изменение правила авторизации, назначенного пространству имен</span><span class="sxs-lookup"><span data-stu-id="bd2a0-123">Example 1: Modify an authorization rule assigned to a namespace</span></span>
```
PS C:\>Set-AzureRmNotificationHubsNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="bd2a0-124">Эта команда изменяет правило авторизации, назначенное пространству имен с именем ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="bd2a0-124">This command modifies an authorization rule assigned to the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="bd2a0-125">Необходимо указать группу ресурсов, которой назначено пространство имен.</span><span class="sxs-lookup"><span data-stu-id="bd2a0-125">You must specify the resource group that the namespace is assigned to.</span></span>
<span data-ttu-id="bd2a0-126">Сведения о правиле авторизации не включаются в саму команду.</span><span class="sxs-lookup"><span data-stu-id="bd2a0-126">Information about the authorization rule is not included in the command itself.</span></span>
<span data-ttu-id="bd2a0-127">Вместо этого эти данные получаются из входного файла C:\Configuration\AuthorizationRules.json.</span><span class="sxs-lookup"><span data-stu-id="bd2a0-127">Instead, that information is obtained from the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="bd2a0-128">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bd2a0-128">PARAMETERS</span></span>

### <span data-ttu-id="bd2a0-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd2a0-129">-DefaultProfile</span></span>
<span data-ttu-id="bd2a0-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bd2a0-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bd2a0-131">-Force</span><span class="sxs-lookup"><span data-stu-id="bd2a0-131">-Force</span></span>
<span data-ttu-id="bd2a0-132">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="bd2a0-132">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="bd2a0-133">-InputFile</span><span class="sxs-lookup"><span data-stu-id="bd2a0-133">-InputFile</span></span>
<span data-ttu-id="bd2a0-134">Задает путь к файлу JSON, содержащему сведения о конфигурации для нового правила.</span><span class="sxs-lookup"><span data-stu-id="bd2a0-134">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

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

### <span data-ttu-id="bd2a0-135">-Namespace</span><span class="sxs-lookup"><span data-stu-id="bd2a0-135">-Namespace</span></span>
<span data-ttu-id="bd2a0-136">Задает пространство имен, содержащее правила авторизации, которые изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="bd2a0-136">Specifies the namespace that contains the authorization rules that this cmdlet modifies.</span></span>
<span data-ttu-id="bd2a0-137">Пространства имен обеспечивают способ группировки и классификации концентраторов уведомлений.</span><span class="sxs-lookup"><span data-stu-id="bd2a0-137">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="bd2a0-138">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bd2a0-138">-ResourceGroup</span></span>
<span data-ttu-id="bd2a0-139">Указывает группу ресурсов, которой назначено пространство имен.</span><span class="sxs-lookup"><span data-stu-id="bd2a0-139">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="bd2a0-140">Группы ресурсов организуют элементы, такие как пространства имен, концентраторы уведомлений и правила авторизации, в целях простого управления запасами и администрирования Azure.</span><span class="sxs-lookup"><span data-stu-id="bd2a0-140">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="bd2a0-141">-SASRule</span><span class="sxs-lookup"><span data-stu-id="bd2a0-141">-SASRule</span></span>
<span data-ttu-id="bd2a0-142">Указывает объект **SharedAccessAuthorizationRuleAttributes** , содержащий сведения о конфигурации для правил авторизации, которые изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="bd2a0-142">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="bd2a0-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bd2a0-143">-Confirm</span></span>
<span data-ttu-id="bd2a0-144">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bd2a0-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd2a0-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd2a0-145">-WhatIf</span></span>
<span data-ttu-id="bd2a0-146">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bd2a0-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bd2a0-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bd2a0-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd2a0-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd2a0-148">CommonParameters</span></span>
<span data-ttu-id="bd2a0-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bd2a0-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd2a0-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd2a0-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd2a0-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bd2a0-151">INPUTS</span></span>

### <span data-ttu-id="bd2a0-152">System. String</span><span class="sxs-lookup"><span data-stu-id="bd2a0-152">System.String</span></span>

## <span data-ttu-id="bd2a0-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd2a0-153">OUTPUTS</span></span>

### <span data-ttu-id="bd2a0-154">Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="bd2a0-154">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="bd2a0-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="bd2a0-155">NOTES</span></span>

## <span data-ttu-id="bd2a0-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bd2a0-156">RELATED LINKS</span></span>

[<span data-ttu-id="bd2a0-157">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="bd2a0-157">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="bd2a0-158">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="bd2a0-158">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./New-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="bd2a0-159">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="bd2a0-159">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubsNamespaceAuthorizationRules.md)


