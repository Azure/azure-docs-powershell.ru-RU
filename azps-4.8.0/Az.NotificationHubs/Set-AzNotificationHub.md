---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F7BBEF57-0DC2-4EFF-9AA2-119B3BD19AE6
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
ms.openlocfilehash: 3dc4a81731f42ce6a27ae5d23fb7c81af76cf789
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078816"
---
# <span data-ttu-id="eac86-101">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="eac86-101">Set-AzNotificationHub</span></span>

## <span data-ttu-id="eac86-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eac86-102">SYNOPSIS</span></span>
<span data-ttu-id="eac86-103">Задает значения свойств для центра уведомлений.</span><span class="sxs-lookup"><span data-stu-id="eac86-103">Sets property values for a notification hub.</span></span>

## <span data-ttu-id="eac86-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eac86-104">SYNTAX</span></span>

### <span data-ttu-id="eac86-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="eac86-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eac86-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="eac86-106">NotificationHubParameterSet</span></span>
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eac86-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eac86-107">DESCRIPTION</span></span>
<span data-ttu-id="eac86-108">Командлет **Set-AzNotificationHub** изменяет значения свойств в центре уведомлений.</span><span class="sxs-lookup"><span data-stu-id="eac86-108">The **Set-AzNotificationHub** cmdlet modifies the property values of a notification hub.</span></span>
<span data-ttu-id="eac86-109">Значение свойства "Центр уведомлений" можно изменить двумя способами.</span><span class="sxs-lookup"><span data-stu-id="eac86-109">You can modify a notification hub property value in two ways.</span></span>
<span data-ttu-id="eac86-110">Для одного из них вы можете создать экземпляр объекта **NotificationHubAttributes** , а затем настроить этот объект с помощью значений свойств, которыми должен обладать новый концентратор.</span><span class="sxs-lookup"><span data-stu-id="eac86-110">For one, you can create an instance of the **NotificationHubAttributes** object and then configure that object with the property values you want the new hub to possess.</span></span>
<span data-ttu-id="eac86-111">Это можно сделать с помощью .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="eac86-111">This can be done through the .NET Framework.</span></span>
<span data-ttu-id="eac86-112">Затем можно скопировать значения этих свойств в центр с помощью параметра *NotificationHubObj* .</span><span class="sxs-lookup"><span data-stu-id="eac86-112">You can then copy those property values to your hub by through the *NotificationHubObj* parameter.</span></span>
<span data-ttu-id="eac86-113">Кроме того, вы можете создать файл JSON (объектная нотация JavaScript), содержащий соответствующие значения конфигурации, а затем применить эти значения через параметр *inputFile* .</span><span class="sxs-lookup"><span data-stu-id="eac86-113">Alternatively, you can create a JSON (JavaScript Object Notation) file that contains the relevant configuration values, then apply those values by through the *InputFile* parameter.</span></span>
<span data-ttu-id="eac86-114">JSON-файл — это текстовый файл, который использует синтаксис, аналогичный приведенному ниже.</span><span class="sxs-lookup"><span data-stu-id="eac86-114">A JSON file is a text file that uses syntax similar to the following: {</span></span>  
    <span data-ttu-id="eac86-115">"Имя": "ContosoNotificationHub";</span><span class="sxs-lookup"><span data-stu-id="eac86-115">"Name": "ContosoNotificationHub",</span></span>  
    <span data-ttu-id="eac86-116">"Расположение": "Западная часть США",</span><span class="sxs-lookup"><span data-stu-id="eac86-116">"Location": "West US",</span></span>  
<span data-ttu-id="eac86-117">} При использовании в сочетании с командлетом **Set-AzNotificationHub** предыдущий пример JSON задает значение расположения концентратора уведомлений с именем ContosoNotificationHub на запад US.</span><span class="sxs-lookup"><span data-stu-id="eac86-117">} When used in conjunction with the **Set-AzNotificationHub** cmdlet, the preceding JSON sample sets the Location value of a notification hub named ContosoNotificationHub to West US.</span></span>

## <span data-ttu-id="eac86-118">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eac86-118">EXAMPLES</span></span>

### <span data-ttu-id="eac86-119">Пример 1: изменение значений свойств для центра уведомлений</span><span class="sxs-lookup"><span data-stu-id="eac86-119">Example 1: Modify the property values for a notification hub</span></span>
```
PS C:\>Set-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\Hubs.json"
```

<span data-ttu-id="eac86-120">Эта команда изменяет значения свойств для центра уведомлений, найденного в пространстве имен ContosoNamespace, и назначает его группе ресурсов ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="eac86-120">This command modifies the property values for a notification hub found in the ContosoNamespace namespace and assigned it to the resource group ContosoNotificationsGroup.</span></span>
<span data-ttu-id="eac86-121">Значения свойства, а также имя узла, который нужно изменить, не указываются в команде.</span><span class="sxs-lookup"><span data-stu-id="eac86-121">The property values, as well as the name of the hub to be modified, are not specified in the command.</span></span>
<span data-ttu-id="eac86-122">Вместо этого информация, содержащаяся в файле ввода, C:\Configuration\Hubs.jsвключена.</span><span class="sxs-lookup"><span data-stu-id="eac86-122">Instead, that information is contained in the input file C:\Configuration\Hubs.json.</span></span>

## <span data-ttu-id="eac86-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eac86-123">PARAMETERS</span></span>

### <span data-ttu-id="eac86-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eac86-124">-DefaultProfile</span></span>
<span data-ttu-id="eac86-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="eac86-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eac86-126">-Force</span><span class="sxs-lookup"><span data-stu-id="eac86-126">-Force</span></span>
<span data-ttu-id="eac86-127">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="eac86-127">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="eac86-128">-InputFile</span><span class="sxs-lookup"><span data-stu-id="eac86-128">-InputFile</span></span>
<span data-ttu-id="eac86-129">Задает путь к файлу JSON, содержащему сведения о конфигурации для центра уведомлений.</span><span class="sxs-lookup"><span data-stu-id="eac86-129">Specifies the path to a JSON file that contains configuration information for the notification hub.</span></span>

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

### <span data-ttu-id="eac86-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="eac86-130">-Namespace</span></span>
<span data-ttu-id="eac86-131">Задает пространство имен, которому назначен Центр уведомлений.</span><span class="sxs-lookup"><span data-stu-id="eac86-131">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="eac86-132">Пространства имен обеспечивают способ группировки и классификации концентраторов уведомлений.</span><span class="sxs-lookup"><span data-stu-id="eac86-132">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="eac86-133">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="eac86-133">-NotificationHubObj</span></span>
<span data-ttu-id="eac86-134">Указывает объект **NotificationHubAttributes** , который содержит сведения о конфигурации для основного центра, измененного этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="eac86-134">Specifies the **NotificationHubAttributes** object that contains configuration information for the hub that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="eac86-135">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="eac86-135">-ResourceGroup</span></span>
<span data-ttu-id="eac86-136">Указывает группу ресурсов, которой назначен Центр уведомлений.</span><span class="sxs-lookup"><span data-stu-id="eac86-136">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="eac86-137">Группы ресурсов организуют элементы, такие как пространства имен, концентраторы уведомлений и правила авторизации, в целях простого управления запасами и администрирования Azure.</span><span class="sxs-lookup"><span data-stu-id="eac86-137">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="eac86-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eac86-138">-Confirm</span></span>
<span data-ttu-id="eac86-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="eac86-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eac86-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eac86-140">-WhatIf</span></span>
<span data-ttu-id="eac86-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="eac86-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eac86-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="eac86-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eac86-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eac86-143">CommonParameters</span></span>
<span data-ttu-id="eac86-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eac86-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eac86-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eac86-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eac86-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eac86-146">INPUTS</span></span>

### <span data-ttu-id="eac86-147">System. String</span><span class="sxs-lookup"><span data-stu-id="eac86-147">System.String</span></span>

## <span data-ttu-id="eac86-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eac86-148">OUTPUTS</span></span>

### <span data-ttu-id="eac86-149">Microsoft. Azure. Commands. NotificationHubs. Models. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="eac86-149">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="eac86-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="eac86-150">NOTES</span></span>

## <span data-ttu-id="eac86-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eac86-151">RELATED LINKS</span></span>

[<span data-ttu-id="eac86-152">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="eac86-152">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="eac86-153">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="eac86-153">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="eac86-154">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="eac86-154">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)


