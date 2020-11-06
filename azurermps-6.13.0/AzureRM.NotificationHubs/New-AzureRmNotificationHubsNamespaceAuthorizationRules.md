---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 3F59F7E8-CD32-40CB-9DE0-3FB044439DD0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/new-azurermnotificationhubsnamespaceauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: 6a55a1b6b032bf2354d7d88699744f9cc5dbaea2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564187"
---
# <span data-ttu-id="d294a-101">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="d294a-101">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>

## <span data-ttu-id="d294a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d294a-102">SYNOPSIS</span></span>
<span data-ttu-id="d294a-103">Создает правило авторизации и назначает это правило пространству имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="d294a-103">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d294a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d294a-104">SYNTAX</span></span>

### <span data-ttu-id="d294a-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="d294a-105">InputFileParameterSet</span></span>
```
New-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d294a-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="d294a-106">SASRuleParameterSet</span></span>
```
New-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d294a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d294a-107">DESCRIPTION</span></span>
<span data-ttu-id="d294a-108">Командлет **New-AzureRmNotificationHubsNamespaceAuthorizationRules** создает правило авторизации для общего доступа к подписи (SAS) и назначает его пространству имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="d294a-108">The **New-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet creates a Shared Access Signature (SAS) authorization rule and assigns it to a notification hub namespace.</span></span>
<span data-ttu-id="d294a-109">Правила авторизации управляют правами пользователей на пространство имен и на концентраторы уведомлений, содержащиеся в этом пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="d294a-109">Authorization rules manage user rights to the namespace and to the notification hubs contained with that namespace.</span></span>
<span data-ttu-id="d294a-110">Этот командлет предоставляет два способа создания нового правила авторизации и назначения его пространству имен.</span><span class="sxs-lookup"><span data-stu-id="d294a-110">This cmdlet provides two ways to create a new authorization rule and assign it to a namespace.</span></span>
<span data-ttu-id="d294a-111">Вы можете создать экземпляр объекта **SharedAccessAuthorizationRuleAttributes** , а затем настроить этот объект с помощью значений свойств, которым должно обладать новое правило.</span><span class="sxs-lookup"><span data-stu-id="d294a-111">You can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the new rule to possess.</span></span>
<span data-ttu-id="d294a-112">Это можно сделать с помощью .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="d294a-112">This can be done using .NET Framework.</span></span>
<span data-ttu-id="d294a-113">Затем вы можете скопировать значения этих свойств в новое правило с помощью параметра *SASRule* .</span><span class="sxs-lookup"><span data-stu-id="d294a-113">You can then copy those property values to your new rule by using *SASRule* parameter.</span></span>
<span data-ttu-id="d294a-114">Кроме того, вы можете создать файл JSON (объектной нотации JavaScript), содержащий соответствующие значения конфигурации, и применить эти значения с помощью параметра *inputFile* .</span><span class="sxs-lookup"><span data-stu-id="d294a-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values by using the *InputFile* parameter.</span></span>
<span data-ttu-id="d294a-115">JSON-файл — это текстовый файл, который использует синтаксис, аналогичный приведенному ниже.</span><span class="sxs-lookup"><span data-stu-id="d294a-115">A JSON file is a text file that uses syntax similar to the following: {</span></span>  
    <span data-ttu-id="d294a-116">"Имя": "ContosoAuthorizationRule";</span><span class="sxs-lookup"><span data-stu-id="d294a-116">"Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="d294a-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =";</span><span class="sxs-lookup"><span data-stu-id="d294a-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="d294a-118">"Права": \[</span><span class="sxs-lookup"><span data-stu-id="d294a-118">"Rights": \[</span></span>  
        <span data-ttu-id="d294a-119">"Прослушать",</span><span class="sxs-lookup"><span data-stu-id="d294a-119">"Listen",</span></span>  
        <span data-ttu-id="d294a-120">Отправить</span><span class="sxs-lookup"><span data-stu-id="d294a-120">"Send"</span></span>  
    \]  
<span data-ttu-id="d294a-121">} При использовании в сочетании с командлетом **New-AzureRmNotificationHubsNamespaceAuthorizationRules** предыдущий пример JSON создает правило авторизации с именем ContosoAuthorizationRule, которое дает пользователям возможность прослушивать и отправлять права в пространство имен.</span><span class="sxs-lookup"><span data-stu-id="d294a-121">} When used in conjunction with the **New-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet, the preceding JSON sample creates an authorization rule named ContosoAuthorizationRule that gives users Listen and Send rights to the namespace.</span></span>
<span data-ttu-id="d294a-122">Значение *PrimaryKey* , используемое для проверки подлинности, может быть сгенерировано случайным образом с помощью следующей команды Windows PowerShell: \[ Convert \] :: ToBase64String ((1.. 32 |% { \[ Byte/] (Get-Minimum-минимум 0-Maximum 255)}))</span><span class="sxs-lookup"><span data-stu-id="d294a-122">The *PrimaryKey* that is used for authentication, can be randomly generated by using the following Windows PowerShell command: \[Convert\]::ToBase64String((1..32 |% { \[byte/](Get-Random -Minimum 0 -Maximum 255) }))</span></span>

## <span data-ttu-id="d294a-123">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d294a-123">EXAMPLES</span></span>

### <span data-ttu-id="d294a-124">Пример 1: Создание правила авторизации и назначение его пространству имен</span><span class="sxs-lookup"><span data-stu-id="d294a-124">Example 1: Create an authorization rule and assign it to a namespace</span></span>
```
PS C:\>New-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\NamespaceAuthorizationRules.json"
```

<span data-ttu-id="d294a-125">Эта команда создает правило авторизации и назначает это правило для пространства имен ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="d294a-125">This command creates an authorization rule and assigns that rule to the namespace ContosoNamespace.</span></span>
<span data-ttu-id="d294a-126">При создании этого правила необходимо указать соответствующее пространство имен и группу ресурсов, которой назначено пространство имен.</span><span class="sxs-lookup"><span data-stu-id="d294a-126">When creating this rule you must specify the appropriate namespace and the resource group that the namespace is assigned to.</span></span>
<span data-ttu-id="d294a-127">Однако вам не нужно указывать сведения о правиле: сведения о правиле будут взяты из входного файла C:\Configuration\NamespaceAuthorizationRules.json.</span><span class="sxs-lookup"><span data-stu-id="d294a-127">However, you do not need to specify any information about the rule itself: rule information will be taken from the input file C:\Configuration\NamespaceAuthorizationRules.json.</span></span>

## <span data-ttu-id="d294a-128">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d294a-128">PARAMETERS</span></span>

### <span data-ttu-id="d294a-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d294a-129">-DefaultProfile</span></span>
<span data-ttu-id="d294a-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d294a-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d294a-131">-InputFile</span><span class="sxs-lookup"><span data-stu-id="d294a-131">-InputFile</span></span>
<span data-ttu-id="d294a-132">Задает путь к файлу JSON, содержащему сведения о конфигурации для нового правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="d294a-132">Specifies the path to a JSON file containing configuration information for the new authorization rule.</span></span>

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

### <span data-ttu-id="d294a-133">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d294a-133">-Namespace</span></span>
<span data-ttu-id="d294a-134">Задает пространство имен, которому будут назначены правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="d294a-134">Specifies the namespace to which the authorization rules will be assigned.</span></span>
<span data-ttu-id="d294a-135">Пространства имен обеспечивают способ группировки и классификации концентраторов уведомлений.</span><span class="sxs-lookup"><span data-stu-id="d294a-135">Namespaces provide a way to group and categorize notification hubs.</span></span>
<span data-ttu-id="d294a-136">Новые правила должны быть назначены существующему пространству имен.</span><span class="sxs-lookup"><span data-stu-id="d294a-136">The new rules must be assigned to an existing namespace.</span></span>
<span data-ttu-id="d294a-137">Командлет **New-AzureRmNotificationHubsNamespaceAuthorizationRules** не может создать новое пространство имен.</span><span class="sxs-lookup"><span data-stu-id="d294a-137">The **New-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet cannot create a new namespace.</span></span>

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

### <span data-ttu-id="d294a-138">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d294a-138">-ResourceGroup</span></span>
<span data-ttu-id="d294a-139">Указывает группу ресурсов, которой назначено пространство имен.</span><span class="sxs-lookup"><span data-stu-id="d294a-139">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="d294a-140">Группы ресурсов организуют элементы, такие как пространства имен, концентраторы уведомлений и правила авторизации, в целях простого управления запасами и администрирования Azure.</span><span class="sxs-lookup"><span data-stu-id="d294a-140">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>
<span data-ttu-id="d294a-141">Необходимо использовать существующую группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d294a-141">You must use an existing resource group.</span></span>
<span data-ttu-id="d294a-142">Этот командлет не может создать новую группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d294a-142">This cmdlet cannot create a new resource group.</span></span>

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

### <span data-ttu-id="d294a-143">-SASRule</span><span class="sxs-lookup"><span data-stu-id="d294a-143">-SASRule</span></span>
<span data-ttu-id="d294a-144">Указывает объект **SharedAccessAuthorizationRuleAttributes** , содержащий сведения о конфигурации для новых правил.</span><span class="sxs-lookup"><span data-stu-id="d294a-144">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

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

### <span data-ttu-id="d294a-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d294a-145">-Confirm</span></span>
<span data-ttu-id="d294a-146">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d294a-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d294a-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d294a-147">-WhatIf</span></span>
<span data-ttu-id="d294a-148">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d294a-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d294a-149">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d294a-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d294a-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d294a-150">CommonParameters</span></span>
<span data-ttu-id="d294a-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d294a-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d294a-152">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d294a-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d294a-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d294a-153">INPUTS</span></span>

### <span data-ttu-id="d294a-154">System. String</span><span class="sxs-lookup"><span data-stu-id="d294a-154">System.String</span></span>

## <span data-ttu-id="d294a-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d294a-155">OUTPUTS</span></span>

### <span data-ttu-id="d294a-156">Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="d294a-156">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="d294a-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="d294a-157">NOTES</span></span>

## <span data-ttu-id="d294a-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d294a-158">RELATED LINKS</span></span>

[<span data-ttu-id="d294a-159">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="d294a-159">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="d294a-160">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="d294a-160">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="d294a-161">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="d294a-161">Set-AzureRmNotificationHubAuthorizationRules</span></span>](./Set-AzureRmNotificationHubAuthorizationRules.md)


