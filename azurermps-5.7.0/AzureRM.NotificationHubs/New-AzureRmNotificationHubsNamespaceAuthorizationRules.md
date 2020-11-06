---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 3F59F7E8-CD32-40CB-9DE0-3FB044439DD0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/new-azurermnotificationhubsnamespaceauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: 2530d4b0075856b6a172bdcf104474d320f657bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567431"
---
# <span data-ttu-id="2fd8b-101">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="2fd8b-101">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>

## <span data-ttu-id="2fd8b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2fd8b-102">SYNOPSIS</span></span>
<span data-ttu-id="2fd8b-103">Создает правило авторизации и назначает это правило пространству имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="2fd8b-103">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2fd8b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2fd8b-104">SYNTAX</span></span>

### <span data-ttu-id="2fd8b-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fd8b-105">InputFileParameterSet</span></span>
```
New-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fd8b-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fd8b-106">SASRuleParameterSet</span></span>
```
New-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fd8b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2fd8b-107">DESCRIPTION</span></span>
<span data-ttu-id="2fd8b-108">Командлет **New-AzureRmNotificationHubsNamespaceAuthorizationRules** создает правило авторизации для общего доступа к подписи (SAS) и назначает его пространству имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="2fd8b-108">The **New-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet creates a Shared Access Signature (SAS) authorization rule and assigns it to a notification hub namespace.</span></span>
<span data-ttu-id="2fd8b-109">Правила авторизации управляют правами пользователей на пространство имен и на концентраторы уведомлений, содержащиеся в этом пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="2fd8b-109">Authorization rules manage user rights to the namespace and to the notification hubs contained with that namespace.</span></span>

<span data-ttu-id="2fd8b-110">Этот командлет предоставляет два способа создания нового правила авторизации и назначения его пространству имен.</span><span class="sxs-lookup"><span data-stu-id="2fd8b-110">This cmdlet provides two ways to create a new authorization rule and assign it to a namespace.</span></span>
<span data-ttu-id="2fd8b-111">Вы можете создать экземпляр объекта **SharedAccessAuthorizationRuleAttributes** , а затем настроить этот объект с помощью значений свойств, которым должно обладать новое правило.</span><span class="sxs-lookup"><span data-stu-id="2fd8b-111">You can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the new rule to possess.</span></span>
<span data-ttu-id="2fd8b-112">Это можно сделать с помощью .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="2fd8b-112">This can be done using .NET Framework.</span></span>
<span data-ttu-id="2fd8b-113">Затем вы можете скопировать значения этих свойств в новое правило с помощью параметра *SASRule* .</span><span class="sxs-lookup"><span data-stu-id="2fd8b-113">You can then copy those property values to your new rule by using *SASRule* parameter.</span></span>

<span data-ttu-id="2fd8b-114">Кроме того, вы можете создать файл JSON (объектной нотации JavaScript), содержащий соответствующие значения конфигурации, и применить эти значения с помощью параметра *inputFile* .</span><span class="sxs-lookup"><span data-stu-id="2fd8b-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values by using the *InputFile* parameter.</span></span>
<span data-ttu-id="2fd8b-115">JSON-файл — это текстовый файл, который использует синтаксис, аналогичный приведенному ниже.</span><span class="sxs-lookup"><span data-stu-id="2fd8b-115">A JSON file is a text file that uses syntax similar to the following:</span></span>

<span data-ttu-id="2fd8b-116">{</span><span class="sxs-lookup"><span data-stu-id="2fd8b-116">{</span></span>  
    <span data-ttu-id="2fd8b-117">"Имя": "ContosoAuthorizationRule";</span><span class="sxs-lookup"><span data-stu-id="2fd8b-117">"Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="2fd8b-118">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =";</span><span class="sxs-lookup"><span data-stu-id="2fd8b-118">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="2fd8b-119">"Права": \[</span><span class="sxs-lookup"><span data-stu-id="2fd8b-119">"Rights": \[</span></span>  
        <span data-ttu-id="2fd8b-120">"Прослушать",</span><span class="sxs-lookup"><span data-stu-id="2fd8b-120">"Listen",</span></span>  
        <span data-ttu-id="2fd8b-121">Отправить</span><span class="sxs-lookup"><span data-stu-id="2fd8b-121">"Send"</span></span>  
    \]  
<span data-ttu-id="2fd8b-122">}</span><span class="sxs-lookup"><span data-stu-id="2fd8b-122">}</span></span>

<span data-ttu-id="2fd8b-123">При использовании в сочетании с командлетом **New-AzureRmNotificationHubsNamespaceAuthorizationRules** предыдущий пример JSON создает правило авторизации с именем ContosoAuthorizationRule, которое дает пользователям возможность прослушивать и отправлять права в пространство имен.</span><span class="sxs-lookup"><span data-stu-id="2fd8b-123">When used in conjunction with the **New-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet, the preceding JSON sample creates an authorization rule named ContosoAuthorizationRule that gives users Listen and Send rights to the namespace.</span></span>
<span data-ttu-id="2fd8b-124">Значение *PrimaryKey* , используемое для проверки подлинности, может быть создано случайным образом с помощью следующей команды Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="2fd8b-124">The *PrimaryKey* that is used for authentication, can be randomly generated by using the following Windows PowerShell command:</span></span>

<span data-ttu-id="2fd8b-125">\[Convert \] :: ToBase64String ((1.. 32 |% { \[ Byte/]) (Get-Minimum-минимум 0 – максимум 255)}))</span><span class="sxs-lookup"><span data-stu-id="2fd8b-125">\[Convert\]::ToBase64String((1..32 |% { \[byte/](Get-Random -Minimum 0 -Maximum 255) }))</span></span>

## <span data-ttu-id="2fd8b-126">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2fd8b-126">EXAMPLES</span></span>

### <span data-ttu-id="2fd8b-127">Пример 1: Создание правила авторизации и назначение его пространству имен</span><span class="sxs-lookup"><span data-stu-id="2fd8b-127">Example 1: Create an authorization rule and assign it to a namespace</span></span>
```
PS C:\>New-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\NamespaceAuthorizationRules.json"
```

<span data-ttu-id="2fd8b-128">Эта команда создает правило авторизации и назначает это правило для пространства имен ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="2fd8b-128">This command creates an authorization rule and assigns that rule to the namespace ContosoNamespace.</span></span>
<span data-ttu-id="2fd8b-129">При создании этого правила необходимо указать соответствующее пространство имен и группу ресурсов, которой назначено пространство имен.</span><span class="sxs-lookup"><span data-stu-id="2fd8b-129">When creating this rule you must specify the appropriate namespace and the resource group that the namespace is assigned to.</span></span>
<span data-ttu-id="2fd8b-130">Однако вам не нужно указывать сведения о правиле: сведения о правиле будут взяты из входного файла C:\Configuration\NamespaceAuthorizationRules.json.</span><span class="sxs-lookup"><span data-stu-id="2fd8b-130">However, you do not need to specify any information about the rule itself: rule information will be taken from the input file C:\Configuration\NamespaceAuthorizationRules.json.</span></span>

## <span data-ttu-id="2fd8b-131">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2fd8b-131">PARAMETERS</span></span>

### <span data-ttu-id="2fd8b-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fd8b-132">-DefaultProfile</span></span>
<span data-ttu-id="2fd8b-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2fd8b-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2fd8b-134">-InputFile</span><span class="sxs-lookup"><span data-stu-id="2fd8b-134">-InputFile</span></span>
<span data-ttu-id="2fd8b-135">Задает путь к файлу JSON, содержащему сведения о конфигурации для нового правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="2fd8b-135">Specifies the path to a JSON file containing configuration information for the new authorization rule.</span></span>

```yaml
Type: String
Parameter Sets: InputFileParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fd8b-136">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2fd8b-136">-Namespace</span></span>
<span data-ttu-id="2fd8b-137">Задает пространство имен, которому будут назначены правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="2fd8b-137">Specifies the namespace to which the authorization rules will be assigned.</span></span>

<span data-ttu-id="2fd8b-138">Пространства имен обеспечивают способ группировки и классификации концентраторов уведомлений.</span><span class="sxs-lookup"><span data-stu-id="2fd8b-138">Namespaces provide a way to group and categorize notification hubs.</span></span>
<span data-ttu-id="2fd8b-139">Новые правила должны быть назначены существующему пространству имен.</span><span class="sxs-lookup"><span data-stu-id="2fd8b-139">The new rules must be assigned to an existing namespace.</span></span>
<span data-ttu-id="2fd8b-140">Командлет **New-AzureRmNotificationHubsNamespaceAuthorizationRules** не может создать новое пространство имен.</span><span class="sxs-lookup"><span data-stu-id="2fd8b-140">The **New-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet cannot create a new namespace.</span></span>

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

### <span data-ttu-id="2fd8b-141">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2fd8b-141">-ResourceGroup</span></span>
<span data-ttu-id="2fd8b-142">Указывает группу ресурсов, которой назначено пространство имен.</span><span class="sxs-lookup"><span data-stu-id="2fd8b-142">Specifies the resource group to which the namespace is assigned.</span></span>

<span data-ttu-id="2fd8b-143">Группы ресурсов организуют элементы, такие как пространства имен, концентраторы уведомлений и правила авторизации, в целях простого управления запасами и администрирования Azure.</span><span class="sxs-lookup"><span data-stu-id="2fd8b-143">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

<span data-ttu-id="2fd8b-144">Необходимо использовать существующую группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2fd8b-144">You must use an existing resource group.</span></span>
<span data-ttu-id="2fd8b-145">Этот командлет не может создать новую группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2fd8b-145">This cmdlet cannot create a new resource group.</span></span>

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

### <span data-ttu-id="2fd8b-146">-SASRule</span><span class="sxs-lookup"><span data-stu-id="2fd8b-146">-SASRule</span></span>
<span data-ttu-id="2fd8b-147">Указывает объект **SharedAccessAuthorizationRuleAttributes** , содержащий сведения о конфигурации для новых правил.</span><span class="sxs-lookup"><span data-stu-id="2fd8b-147">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

```yaml
Type: SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fd8b-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2fd8b-148">-Confirm</span></span>
<span data-ttu-id="2fd8b-149">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2fd8b-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fd8b-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fd8b-150">-WhatIf</span></span>
<span data-ttu-id="2fd8b-151">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2fd8b-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2fd8b-152">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2fd8b-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fd8b-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fd8b-153">CommonParameters</span></span>
<span data-ttu-id="2fd8b-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2fd8b-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fd8b-155">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fd8b-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fd8b-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2fd8b-156">INPUTS</span></span>

### <span data-ttu-id="2fd8b-157">Ничего</span><span class="sxs-lookup"><span data-stu-id="2fd8b-157">None</span></span>
<span data-ttu-id="2fd8b-158">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="2fd8b-158">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2fd8b-159">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2fd8b-159">OUTPUTS</span></span>

### <span data-ttu-id="2fd8b-160">Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="2fd8b-160">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="2fd8b-161">Пуск</span><span class="sxs-lookup"><span data-stu-id="2fd8b-161">NOTES</span></span>

## <span data-ttu-id="2fd8b-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2fd8b-162">RELATED LINKS</span></span>

[<span data-ttu-id="2fd8b-163">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="2fd8b-163">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="2fd8b-164">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="2fd8b-164">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="2fd8b-165">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="2fd8b-165">Set-AzureRmNotificationHubAuthorizationRules</span></span>](./Set-AzureRmNotificationHubAuthorizationRules.md)


