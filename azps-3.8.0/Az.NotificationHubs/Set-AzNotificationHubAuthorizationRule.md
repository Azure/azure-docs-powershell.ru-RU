---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: BD311CEF-378B-463E-8998-CC3E9A5B3A7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: f95b016380f640154533f69d3942b8fe12a064d7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072767"
---
# <span data-ttu-id="3d5e9-101">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3d5e9-101">Set-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="3d5e9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3d5e9-102">SYNOPSIS</span></span>
<span data-ttu-id="3d5e9-103">Задает правила авторизации для центра уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3d5e9-103">Sets authorization rules for a notification hub.</span></span>

## <span data-ttu-id="3d5e9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3d5e9-104">SYNTAX</span></span>

### <span data-ttu-id="3d5e9-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d5e9-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d5e9-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d5e9-106">SASRuleParameterSet</span></span>
```
Set-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d5e9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d5e9-107">DESCRIPTION</span></span>
<span data-ttu-id="3d5e9-108">Командлет **Set-AzNotificationHubAuthorizationRule** изменяет правило авторизации подписи общего доступа (SAS), назначенное для концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3d5e9-108">The **Set-AzNotificationHubAuthorizationRule** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub.</span></span>
<span data-ttu-id="3d5e9-109">Правила авторизации управляют доступом к концентраторам уведомлений с помощью создания ссылок в виде URI, основанных на различных уровнях разрешений.</span><span class="sxs-lookup"><span data-stu-id="3d5e9-109">Authorization rules manage access to your notification hubs by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="3d5e9-110">Уровни разрешений могут быть одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="3d5e9-110">Permission levels can be one of the following:</span></span> 
- <span data-ttu-id="3d5e9-111">Прослушивающих</span><span class="sxs-lookup"><span data-stu-id="3d5e9-111">Listen</span></span>
- <span data-ttu-id="3d5e9-112">Отправить</span><span class="sxs-lookup"><span data-stu-id="3d5e9-112">Send</span></span>
- <span data-ttu-id="3d5e9-113">Управление клиентами направляется на один из этих URI на основе соответствующего уровня разрешений.</span><span class="sxs-lookup"><span data-stu-id="3d5e9-113">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="3d5e9-114">Например, клиент, которому предоставлено разрешение прослушивания, будет направлен на универсальный код ресурса (URI) для этого разрешения.</span><span class="sxs-lookup"><span data-stu-id="3d5e9-114">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="3d5e9-115">Этот командлет предоставляет два способа изменения правила авторизации, назначенного концентратору уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3d5e9-115">This cmdlet provides two ways to modify an authorization rule assigned to a notification hub.</span></span>
<span data-ttu-id="3d5e9-116">Для одного из них вы можете создать экземпляр объекта **SharedAccessAuthorizationRuleAttributes** , а затем настроить этот объект с помощью значений свойств, которым должно обладать правило.</span><span class="sxs-lookup"><span data-stu-id="3d5e9-116">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="3d5e9-117">Вы можете настроить объект с помощью .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="3d5e9-117">You can configure the object through the .NET Framework.</span></span>
<span data-ttu-id="3d5e9-118">Затем вы можете скопировать значения этих свойств в свое правило с помощью параметра *SASRule* .</span><span class="sxs-lookup"><span data-stu-id="3d5e9-118">You can then copy those property values to your rule by using *SASRule* parameter.</span></span>
<span data-ttu-id="3d5e9-119">Кроме того, вы можете создать файл JSON (объектной нотации JavaScript), содержащий соответствующие значения конфигурации, и применить эти значения с помощью параметра *inputFile* .</span><span class="sxs-lookup"><span data-stu-id="3d5e9-119">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="3d5e9-120">JSON-файл — это текстовый файл, в котором используются такие же синтаксисы: {"Name": "ContosoAuthorizationRule";</span><span class="sxs-lookup"><span data-stu-id="3d5e9-120">A JSON file is a text file that uses syntax similar to this: {      "Name": "ContosoAuthorizationRule",</span></span>  
  <span data-ttu-id="3d5e9-121">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =";</span><span class="sxs-lookup"><span data-stu-id="3d5e9-121">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
  <span data-ttu-id="3d5e9-122">"Права": \[</span><span class="sxs-lookup"><span data-stu-id="3d5e9-122">"Rights": \[</span></span>  
        <span data-ttu-id="3d5e9-123">"Прослушать",</span><span class="sxs-lookup"><span data-stu-id="3d5e9-123">"Listen",</span></span>  
        <span data-ttu-id="3d5e9-124">Отправить</span><span class="sxs-lookup"><span data-stu-id="3d5e9-124">"Send"</span></span>  
    \]  
  <span data-ttu-id="3d5e9-125">} При использовании в сочетании с командлетом New-AzNotificationHubAuthorizationRule предыдущий пример JSON изменяет правило авторизации с именем ContosoAuthorizationRule, чтобы дать пользователям возможность прослушивать и отправлять им права на доступ к концентратору.</span><span class="sxs-lookup"><span data-stu-id="3d5e9-125">} When used in conjunction with the New-AzNotificationHubAuthorizationRule cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule in order to give users Listen and Send rights to the hub.</span></span>

## <span data-ttu-id="3d5e9-126">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3d5e9-126">EXAMPLES</span></span>

### <span data-ttu-id="3d5e9-127">Пример 1: изменение правила авторизации, назначенного концентратору уведомлений</span><span class="sxs-lookup"><span data-stu-id="3d5e9-127">Example 1: Modify an authorization rule assigned to a notification hub</span></span>
```
PS C:\>Set-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -NotificationHub "ContosoExternalHub" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="3d5e9-128">Эта команда изменяет правило авторизации, назначенное концентратору уведомлений с именем ContosoExternalHub.</span><span class="sxs-lookup"><span data-stu-id="3d5e9-128">This command modifies an authorization rule assigned to the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="3d5e9-129">Необходимо указать пространство имен, в котором расположен Центральный центр, а также группу ресурсов, которой назначен концентратор.</span><span class="sxs-lookup"><span data-stu-id="3d5e9-129">You must specify the namespace where the hub is located as well as the resource group that the hub is assigned.</span></span>
<span data-ttu-id="3d5e9-130">Сведения об изменении правила не включаются в саму команду.</span><span class="sxs-lookup"><span data-stu-id="3d5e9-130">Information about the rule that is modified is not included in the command itself.</span></span>
<span data-ttu-id="3d5e9-131">Вместо этого эти данные находятся в файле ввода C:\Configuration\AuthorizationRules.json.</span><span class="sxs-lookup"><span data-stu-id="3d5e9-131">Instead, that information is found in the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="3d5e9-132">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3d5e9-132">PARAMETERS</span></span>

### <span data-ttu-id="3d5e9-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d5e9-133">-DefaultProfile</span></span>
<span data-ttu-id="3d5e9-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3d5e9-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d5e9-135">-Force</span><span class="sxs-lookup"><span data-stu-id="3d5e9-135">-Force</span></span>
<span data-ttu-id="3d5e9-136">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="3d5e9-136">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="3d5e9-137">-InputFile</span><span class="sxs-lookup"><span data-stu-id="3d5e9-137">-InputFile</span></span>
<span data-ttu-id="3d5e9-138">Задает путь к файлу JSON, содержащему сведения о конфигурации для нового правила.</span><span class="sxs-lookup"><span data-stu-id="3d5e9-138">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

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

### <span data-ttu-id="3d5e9-139">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3d5e9-139">-Namespace</span></span>
<span data-ttu-id="3d5e9-140">Задает пространство имен, которому назначен Центр уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3d5e9-140">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="3d5e9-141">Пространства имен обеспечивают способ группировки и классификации концентраторов уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3d5e9-141">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="3d5e9-142">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="3d5e9-142">-NotificationHub</span></span>
<span data-ttu-id="3d5e9-143">Определяет центр уведомлений, к которому назначены правила авторизации с помощью этого командлета.</span><span class="sxs-lookup"><span data-stu-id="3d5e9-143">Specifies the notification hub that this cmdlet assigns authorization rules to.</span></span>
<span data-ttu-id="3d5e9-144">Концентраторы уведомлений используются для отправки push-уведомлений нескольким клиентам вне зависимости от того, что используется этими клиентами.</span><span class="sxs-lookup"><span data-stu-id="3d5e9-144">Notification hubs are used to send push notifications to multiple clients regardless of the used by those clients.</span></span>

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

### <span data-ttu-id="3d5e9-145">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3d5e9-145">-ResourceGroup</span></span>
<span data-ttu-id="3d5e9-146">Указывает группу ресурсов, которой назначен Центр уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3d5e9-146">Specifies the resource group to which the notification hub is assigned.</span></span> <span data-ttu-id="3d5e9-147">Группы ресурсов организуют элементы, такие как пространства имен, концентраторы уведомлений и правила авторизации, в целях простого управления запасами и администрирования Azure.</span><span class="sxs-lookup"><span data-stu-id="3d5e9-147">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="3d5e9-148">-SASRule</span><span class="sxs-lookup"><span data-stu-id="3d5e9-148">-SASRule</span></span>
<span data-ttu-id="3d5e9-149">Указывает объект **SharedAccessAuthorizationRuleAttributes** , содержащий сведения о конфигурации для правил авторизации, которые были изменены.</span><span class="sxs-lookup"><span data-stu-id="3d5e9-149">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that are modified.</span></span>

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

### <span data-ttu-id="3d5e9-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3d5e9-150">-Confirm</span></span>
<span data-ttu-id="3d5e9-151">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3d5e9-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d5e9-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d5e9-152">-WhatIf</span></span>
<span data-ttu-id="3d5e9-153">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3d5e9-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3d5e9-154">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3d5e9-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d5e9-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d5e9-155">CommonParameters</span></span>
<span data-ttu-id="3d5e9-156">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3d5e9-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d5e9-157">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d5e9-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d5e9-158">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3d5e9-158">INPUTS</span></span>

### <span data-ttu-id="3d5e9-159">System. String</span><span class="sxs-lookup"><span data-stu-id="3d5e9-159">System.String</span></span>

## <span data-ttu-id="3d5e9-160">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d5e9-160">OUTPUTS</span></span>

### <span data-ttu-id="3d5e9-161">Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="3d5e9-161">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="3d5e9-162">Пуск</span><span class="sxs-lookup"><span data-stu-id="3d5e9-162">NOTES</span></span>

## <span data-ttu-id="3d5e9-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3d5e9-163">RELATED LINKS</span></span>

[<span data-ttu-id="3d5e9-164">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3d5e9-164">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="3d5e9-165">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3d5e9-165">New-AzNotificationHubAuthorizationRule</span></span>](./New-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="3d5e9-166">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3d5e9-166">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)


