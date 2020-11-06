---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: BD311CEF-378B-463E-8998-CC3E9A5B3A7B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/set-azurermnotificationhubauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: 6203c5554dcdbfbd40c861a3f73e1a5947228030
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569891"
---
# <span data-ttu-id="d93fe-101">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="d93fe-101">Set-AzureRmNotificationHubAuthorizationRules</span></span>

## <span data-ttu-id="d93fe-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d93fe-102">SYNOPSIS</span></span>
<span data-ttu-id="d93fe-103">Задает правила авторизации для центра уведомлений.</span><span class="sxs-lookup"><span data-stu-id="d93fe-103">Sets authorization rules for a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d93fe-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d93fe-104">SYNTAX</span></span>

### <span data-ttu-id="d93fe-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="d93fe-105">InputFileParameterSet</span></span>
```
Set-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d93fe-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="d93fe-106">SASRuleParameterSet</span></span>
```
Set-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d93fe-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d93fe-107">DESCRIPTION</span></span>
<span data-ttu-id="d93fe-108">Командлет **Set-AzureRmNotificationHubAuthorizationRules** изменяет правило авторизации подписи общего доступа (SAS), назначенное для концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="d93fe-108">The **Set-AzureRmNotificationHubAuthorizationRules** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub.</span></span>

<span data-ttu-id="d93fe-109">Правила авторизации управляют доступом к концентраторам уведомлений с помощью создания ссылок в виде URI, основанных на различных уровнях разрешений.</span><span class="sxs-lookup"><span data-stu-id="d93fe-109">Authorization rules manage access to your notification hubs by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="d93fe-110">Уровни разрешений могут быть одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="d93fe-110">Permission levels can be one of the following:</span></span> 

- <span data-ttu-id="d93fe-111">Прослушивающих</span><span class="sxs-lookup"><span data-stu-id="d93fe-111">Listen</span></span>
- <span data-ttu-id="d93fe-112">Отправить</span><span class="sxs-lookup"><span data-stu-id="d93fe-112">Send</span></span>
- <span data-ttu-id="d93fe-113">Этими</span><span class="sxs-lookup"><span data-stu-id="d93fe-113">Manage</span></span>

<span data-ttu-id="d93fe-114">Клиенты направляются на один из этих URI на основе соответствующего уровня разрешений.</span><span class="sxs-lookup"><span data-stu-id="d93fe-114">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="d93fe-115">Например, клиент, которому предоставлено разрешение прослушивания, будет направлен на универсальный код ресурса (URI) для этого разрешения.</span><span class="sxs-lookup"><span data-stu-id="d93fe-115">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>

<span data-ttu-id="d93fe-116">Этот командлет предоставляет два способа изменения правила авторизации, назначенного концентратору уведомлений.</span><span class="sxs-lookup"><span data-stu-id="d93fe-116">This cmdlet provides two ways to modify an authorization rule assigned to a notification hub.</span></span>
<span data-ttu-id="d93fe-117">Для одного из них вы можете создать экземпляр объекта **SharedAccessAuthorizationRuleAttributes** , а затем настроить этот объект с помощью значений свойств, которым должно обладать правило.</span><span class="sxs-lookup"><span data-stu-id="d93fe-117">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="d93fe-118">Вы можете настроить объект с помощью .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="d93fe-118">You can configure the object through the .NET Framework.</span></span>
<span data-ttu-id="d93fe-119">Затем вы можете скопировать значения этих свойств в свое правило с помощью параметра *SASRule* .</span><span class="sxs-lookup"><span data-stu-id="d93fe-119">You can then copy those property values to your rule by using *SASRule* parameter.</span></span>

<span data-ttu-id="d93fe-120">Кроме того, вы можете создать файл JSON (объектной нотации JavaScript), содержащий соответствующие значения конфигурации, и применить эти значения с помощью параметра *inputFile* .</span><span class="sxs-lookup"><span data-stu-id="d93fe-120">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="d93fe-121">JSON-файл — это текстовый файл, в котором используются такие же синтаксисы:</span><span class="sxs-lookup"><span data-stu-id="d93fe-121">A JSON file is a text file that uses syntax similar to this:</span></span>

<span data-ttu-id="d93fe-122">{"Имя": "ContosoAuthorizationRule";</span><span class="sxs-lookup"><span data-stu-id="d93fe-122">{      "Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="d93fe-123">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =";</span><span class="sxs-lookup"><span data-stu-id="d93fe-123">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="d93fe-124">"Права": \[</span><span class="sxs-lookup"><span data-stu-id="d93fe-124">"Rights": \[</span></span>  
        <span data-ttu-id="d93fe-125">"Прослушать",</span><span class="sxs-lookup"><span data-stu-id="d93fe-125">"Listen",</span></span>  
        <span data-ttu-id="d93fe-126">Отправить</span><span class="sxs-lookup"><span data-stu-id="d93fe-126">"Send"</span></span>  
    \]  
<span data-ttu-id="d93fe-127">}</span><span class="sxs-lookup"><span data-stu-id="d93fe-127">}</span></span>

<span data-ttu-id="d93fe-128">При использовании в сочетании с командлетом New-AzureRmNotificationHubAuthorizationRules предыдущий пример JSON изменяет правило авторизации с именем ContosoAuthorizationRule, чтобы предоставить пользователям возможность прослушивать и отправлять им права на доступ к концентратору.</span><span class="sxs-lookup"><span data-stu-id="d93fe-128">When used in conjunction with the New-AzureRmNotificationHubAuthorizationRules cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule in order to give users Listen and Send rights to the hub.</span></span>

## <span data-ttu-id="d93fe-129">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d93fe-129">EXAMPLES</span></span>

### <span data-ttu-id="d93fe-130">Пример 1: изменение правила авторизации, назначенного концентратору уведомлений</span><span class="sxs-lookup"><span data-stu-id="d93fe-130">Example 1: Modify an authorization rule assigned to a notification hub</span></span>
```
PS C:\>Set-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -NotificationHub "ContosoExternalHub" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="d93fe-131">Эта команда изменяет правило авторизации, назначенное концентратору уведомлений с именем ContosoExternalHub.</span><span class="sxs-lookup"><span data-stu-id="d93fe-131">This command modifies an authorization rule assigned to the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="d93fe-132">Необходимо указать пространство имен, в котором расположен Центральный центр, а также группу ресурсов, которой назначен концентратор.</span><span class="sxs-lookup"><span data-stu-id="d93fe-132">You must specify the namespace where the hub is located as well as the resource group that the hub is assigned.</span></span>
<span data-ttu-id="d93fe-133">Сведения об изменении правила не включаются в саму команду.</span><span class="sxs-lookup"><span data-stu-id="d93fe-133">Information about the rule that is modified is not included in the command itself.</span></span>
<span data-ttu-id="d93fe-134">Вместо этого эти данные находятся в файле ввода C:\Configuration\AuthorizationRules.json.</span><span class="sxs-lookup"><span data-stu-id="d93fe-134">Instead, that information is found in the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="d93fe-135">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d93fe-135">PARAMETERS</span></span>

### <span data-ttu-id="d93fe-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d93fe-136">-DefaultProfile</span></span>
<span data-ttu-id="d93fe-137">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d93fe-137">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d93fe-138">-Force</span><span class="sxs-lookup"><span data-stu-id="d93fe-138">-Force</span></span>
<span data-ttu-id="d93fe-139">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="d93fe-139">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d93fe-140">-InputFile</span><span class="sxs-lookup"><span data-stu-id="d93fe-140">-InputFile</span></span>
<span data-ttu-id="d93fe-141">Задает путь к файлу JSON, содержащему сведения о конфигурации для нового правила.</span><span class="sxs-lookup"><span data-stu-id="d93fe-141">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

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

### <span data-ttu-id="d93fe-142">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d93fe-142">-Namespace</span></span>
<span data-ttu-id="d93fe-143">Задает пространство имен, которому назначен Центр уведомлений.</span><span class="sxs-lookup"><span data-stu-id="d93fe-143">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="d93fe-144">Пространства имен обеспечивают способ группировки и классификации концентраторов уведомлений.</span><span class="sxs-lookup"><span data-stu-id="d93fe-144">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="d93fe-145">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="d93fe-145">-NotificationHub</span></span>
<span data-ttu-id="d93fe-146">Определяет центр уведомлений, к которому назначены правила авторизации с помощью этого командлета.</span><span class="sxs-lookup"><span data-stu-id="d93fe-146">Specifies the notification hub that this cmdlet assigns authorization rules to.</span></span>
<span data-ttu-id="d93fe-147">Концентраторы уведомлений используются для отправки push-уведомлений нескольким клиентам вне зависимости от того, что используется этими клиентами.</span><span class="sxs-lookup"><span data-stu-id="d93fe-147">Notification hubs are used to send push notifications to multiple clients regardless of the used by those clients.</span></span>

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

### <span data-ttu-id="d93fe-148">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d93fe-148">-ResourceGroup</span></span>
<span data-ttu-id="d93fe-149">Указывает группу ресурсов, которой назначен Центр уведомлений.</span><span class="sxs-lookup"><span data-stu-id="d93fe-149">Specifies the resource group to which the notification hub is assigned.</span></span> <span data-ttu-id="d93fe-150">Группы ресурсов организуют элементы, такие как пространства имен, концентраторы уведомлений и правила авторизации, в целях простого управления запасами и администрирования Azure.</span><span class="sxs-lookup"><span data-stu-id="d93fe-150">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="d93fe-151">-SASRule</span><span class="sxs-lookup"><span data-stu-id="d93fe-151">-SASRule</span></span>
<span data-ttu-id="d93fe-152">Указывает объект **SharedAccessAuthorizationRuleAttributes** , содержащий сведения о конфигурации для правил авторизации, которые были изменены.</span><span class="sxs-lookup"><span data-stu-id="d93fe-152">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that are modified.</span></span>

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

### <span data-ttu-id="d93fe-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d93fe-153">-Confirm</span></span>
<span data-ttu-id="d93fe-154">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d93fe-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d93fe-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d93fe-155">-WhatIf</span></span>
<span data-ttu-id="d93fe-156">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d93fe-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d93fe-157">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d93fe-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d93fe-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d93fe-158">CommonParameters</span></span>
<span data-ttu-id="d93fe-159">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d93fe-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d93fe-160">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d93fe-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d93fe-161">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d93fe-161">INPUTS</span></span>

### <span data-ttu-id="d93fe-162">Ничего</span><span class="sxs-lookup"><span data-stu-id="d93fe-162">None</span></span>
<span data-ttu-id="d93fe-163">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="d93fe-163">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d93fe-164">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d93fe-164">OUTPUTS</span></span>

### <span data-ttu-id="d93fe-165">Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="d93fe-165">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="d93fe-166">Пуск</span><span class="sxs-lookup"><span data-stu-id="d93fe-166">NOTES</span></span>

## <span data-ttu-id="d93fe-167">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d93fe-167">RELATED LINKS</span></span>

[<span data-ttu-id="d93fe-168">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="d93fe-168">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="d93fe-169">New-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="d93fe-169">New-AzureRmNotificationHubAuthorizationRules</span></span>](./New-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="d93fe-170">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="d93fe-170">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubAuthorizationRules.md)


