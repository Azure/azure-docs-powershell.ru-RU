---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F7BBEF57-0DC2-4EFF-9AA2-119B3BD19AE6
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
ms.openlocfilehash: f59ac6a2e1431c3ba04ff0ac9cf9cafbfdfe367e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904741"
---
# <span data-ttu-id="3ab0d-101">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="3ab0d-101">Set-AzNotificationHub</span></span>

## <span data-ttu-id="3ab0d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3ab0d-102">SYNOPSIS</span></span>
<span data-ttu-id="3ab0d-103">Задает значения свойств для центра уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3ab0d-103">Sets property values for a notification hub.</span></span>

## <span data-ttu-id="3ab0d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3ab0d-104">SYNTAX</span></span>

### <span data-ttu-id="3ab0d-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ab0d-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ab0d-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ab0d-106">NotificationHubParameterSet</span></span>
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ab0d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ab0d-107">DESCRIPTION</span></span>
<span data-ttu-id="3ab0d-108">Командлет **Set-AzNotificationHub** изменяет значения свойств в центре уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3ab0d-108">The **Set-AzNotificationHub** cmdlet modifies the property values of a notification hub.</span></span>
<span data-ttu-id="3ab0d-109">Значение свойства "Центр уведомлений" можно изменить двумя способами.</span><span class="sxs-lookup"><span data-stu-id="3ab0d-109">You can modify a notification hub property value in two ways.</span></span>
<span data-ttu-id="3ab0d-110">Для одного из них вы можете создать экземпляр объекта **NotificationHubAttributes** , а затем настроить этот объект с помощью значений свойств, которыми должен обладать новый концентратор.</span><span class="sxs-lookup"><span data-stu-id="3ab0d-110">For one, you can create an instance of the **NotificationHubAttributes** object and then configure that object with the property values you want the new hub to possess.</span></span>
<span data-ttu-id="3ab0d-111">Это можно сделать с помощью .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="3ab0d-111">This can be done through the .NET Framework.</span></span>
<span data-ttu-id="3ab0d-112">Затем можно скопировать значения этих свойств в центр с помощью параметра *NotificationHubObj* .</span><span class="sxs-lookup"><span data-stu-id="3ab0d-112">You can then copy those property values to your hub by through the *NotificationHubObj* parameter.</span></span>
<span data-ttu-id="3ab0d-113">Кроме того, вы можете создать файл JSON (объектная нотация JavaScript), содержащий соответствующие значения конфигурации, а затем применить эти значения через параметр *inputFile* .</span><span class="sxs-lookup"><span data-stu-id="3ab0d-113">Alternatively, you can create a JSON (JavaScript Object Notation) file that contains the relevant configuration values, then apply those values by through the *InputFile* parameter.</span></span>
<span data-ttu-id="3ab0d-114">JSON-файл — это текстовый файл, который использует синтаксис, аналогичный приведенному ниже.</span><span class="sxs-lookup"><span data-stu-id="3ab0d-114">A JSON file is a text file that uses syntax similar to the following: {</span></span>  
    <span data-ttu-id="3ab0d-115">"Имя": "ContosoNotificationHub";</span><span class="sxs-lookup"><span data-stu-id="3ab0d-115">"Name": "ContosoNotificationHub",</span></span>  
    <span data-ttu-id="3ab0d-116">"Расположение": "Западная часть США",</span><span class="sxs-lookup"><span data-stu-id="3ab0d-116">"Location": "West US",</span></span>  
<span data-ttu-id="3ab0d-117">} При использовании в сочетании с командлетом **Set-AzNotificationHub** предыдущий пример JSON задает значение расположения концентратора уведомлений с именем ContosoNotificationHub на запад US.</span><span class="sxs-lookup"><span data-stu-id="3ab0d-117">} When used in conjunction with the **Set-AzNotificationHub** cmdlet, the preceding JSON sample sets the Location value of a notification hub named ContosoNotificationHub to West US.</span></span>

## <span data-ttu-id="3ab0d-118">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3ab0d-118">EXAMPLES</span></span>

### <span data-ttu-id="3ab0d-119">Пример 1: изменение значений свойств для центра уведомлений</span><span class="sxs-lookup"><span data-stu-id="3ab0d-119">Example 1: Modify the property values for a notification hub</span></span>
```
PS C:\>Set-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\Hubs.json"
```

<span data-ttu-id="3ab0d-120">Эта команда изменяет значения свойств для центра уведомлений, найденного в пространстве имен ContosoNamespace, и назначает его группе ресурсов ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="3ab0d-120">This command modifies the property values for a notification hub found in the ContosoNamespace namespace and assigned it to the resource group ContosoNotificationsGroup.</span></span>
<span data-ttu-id="3ab0d-121">Значения свойства, а также имя узла, который нужно изменить, не указываются в команде.</span><span class="sxs-lookup"><span data-stu-id="3ab0d-121">The property values, as well as the name of the hub to be modified, are not specified in the command.</span></span>
<span data-ttu-id="3ab0d-122">Вместо этого информация, содержащаяся в файле ввода, C:\Configuration\Hubs.jsвключена.</span><span class="sxs-lookup"><span data-stu-id="3ab0d-122">Instead, that information is contained in the input file C:\Configuration\Hubs.json.</span></span>

## <span data-ttu-id="3ab0d-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3ab0d-123">PARAMETERS</span></span>

### <span data-ttu-id="3ab0d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ab0d-124">-DefaultProfile</span></span>
<span data-ttu-id="3ab0d-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3ab0d-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3ab0d-126">-Force</span><span class="sxs-lookup"><span data-stu-id="3ab0d-126">-Force</span></span>
<span data-ttu-id="3ab0d-127">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="3ab0d-127">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="3ab0d-128">-InputFile</span><span class="sxs-lookup"><span data-stu-id="3ab0d-128">-InputFile</span></span>
<span data-ttu-id="3ab0d-129">Задает путь к файлу JSON, содержащему сведения о конфигурации для центра уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3ab0d-129">Specifies the path to a JSON file that contains configuration information for the notification hub.</span></span>

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

### <span data-ttu-id="3ab0d-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3ab0d-130">-Namespace</span></span>
<span data-ttu-id="3ab0d-131">Задает пространство имен, которому назначен Центр уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3ab0d-131">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="3ab0d-132">Пространства имен обеспечивают способ группировки и классификации концентраторов уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3ab0d-132">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="3ab0d-133">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="3ab0d-133">-NotificationHubObj</span></span>
<span data-ttu-id="3ab0d-134">Указывает объект **NotificationHubAttributes** , который содержит сведения о конфигурации для основного центра, измененного этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="3ab0d-134">Specifies the **NotificationHubAttributes** object that contains configuration information for the hub that this cmdlet modifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes
Parameter Sets: NotificationHubParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ab0d-135">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3ab0d-135">-ResourceGroup</span></span>
<span data-ttu-id="3ab0d-136">Указывает группу ресурсов, которой назначен Центр уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3ab0d-136">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="3ab0d-137">Группы ресурсов организуют элементы, такие как пространства имен, концентраторы уведомлений и правила авторизации, в целях простого управления запасами и администрирования Azure.</span><span class="sxs-lookup"><span data-stu-id="3ab0d-137">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="3ab0d-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3ab0d-138">-Confirm</span></span>
<span data-ttu-id="3ab0d-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3ab0d-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ab0d-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ab0d-140">-WhatIf</span></span>
<span data-ttu-id="3ab0d-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3ab0d-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3ab0d-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3ab0d-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ab0d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ab0d-143">CommonParameters</span></span>
<span data-ttu-id="3ab0d-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3ab0d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ab0d-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ab0d-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ab0d-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3ab0d-146">INPUTS</span></span>

### <span data-ttu-id="3ab0d-147">System. String</span><span class="sxs-lookup"><span data-stu-id="3ab0d-147">System.String</span></span>

## <span data-ttu-id="3ab0d-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ab0d-148">OUTPUTS</span></span>

### <span data-ttu-id="3ab0d-149">Microsoft. Azure. Commands. NotificationHubs. Models. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="3ab0d-149">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="3ab0d-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="3ab0d-150">NOTES</span></span>

## <span data-ttu-id="3ab0d-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3ab0d-151">RELATED LINKS</span></span>

[<span data-ttu-id="3ab0d-152">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="3ab0d-152">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="3ab0d-153">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="3ab0d-153">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="3ab0d-154">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="3ab0d-154">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)


