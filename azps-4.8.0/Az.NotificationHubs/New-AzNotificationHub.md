---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 8EDDA991-55B6-4151-8619-E13E14599ECD
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHub.md
ms.openlocfilehash: 3fb98dc1ef4b13b87fc7cfa41e165d9bc24fc17c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244755"
---
# <span data-ttu-id="77666-101">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="77666-101">New-AzNotificationHub</span></span>

## <span data-ttu-id="77666-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="77666-102">SYNOPSIS</span></span>
<span data-ttu-id="77666-103">Создает концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="77666-103">Creates a notification hub.</span></span>

## <span data-ttu-id="77666-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="77666-104">SYNTAX</span></span>

### <span data-ttu-id="77666-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="77666-105">InputFileParameterSet</span></span>
```
New-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77666-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="77666-106">NotificationHubParameterSet</span></span>
```
New-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77666-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="77666-107">DESCRIPTION</span></span>
<span data-ttu-id="77666-108">Командлет **New-AzNotificationHub** создает концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="77666-108">The **New-AzNotificationHub** cmdlet creates a notification hub.</span></span>
<span data-ttu-id="77666-109">Концентраторы уведомлений используются для отправки push-уведомлений нескольким клиентам вне зависимости от платформы, используемой этими клиентами.</span><span class="sxs-lookup"><span data-stu-id="77666-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="77666-110">Концентраторы уведомлений примерно эквивалентны отдельным приложениям: каждое из ваших приложений обычно имеет собственный концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="77666-110">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="77666-111">Командлет **New-AzNotificationHub** предоставляет два способа создания нового концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="77666-111">The **New-AzNotificationHub** cmdlet provides two ways to create a new notification hub.</span></span>
<span data-ttu-id="77666-112">Вы можете создать экземпляр объекта **NotificationHubAttributes** , а затем настроить этот объект.</span><span class="sxs-lookup"><span data-stu-id="77666-112">You can create an instance of the **NotificationHubAttributes** object and then configure that object.</span></span>
<span data-ttu-id="77666-113">Затем вы можете скопировать значения этих свойств в новый центр с помощью параметра *NotificationHubObj* .</span><span class="sxs-lookup"><span data-stu-id="77666-113">You can then copy those property values to your new hub by through the *NotificationHubObj* parameter.</span></span>
<span data-ttu-id="77666-114">Кроме того, вы можете создать файл JSON (объектной нотации JavaScript), содержащий соответствующие значения конфигурации, и применить эти значения с помощью параметра *inputFile* .</span><span class="sxs-lookup"><span data-stu-id="77666-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and  then apply those values by using the *InputFile* parameter.</span></span>
<span data-ttu-id="77666-115">При использовании в сочетании с командлетом **New-AzNotificationHub** в ПРЕДЫДУЩЕМ примере JSON создается центр уведомлений под названием ContosoNotificationHub, который находится в центре обработки данных "Западная часть США".</span><span class="sxs-lookup"><span data-stu-id="77666-115">When used in conjunction with the **New-AzNotificationHub** cmdlet, the preceding JSON sample creates a notification hub named ContosoNotificationHub located on the West US datacenter.</span></span>

## <span data-ttu-id="77666-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="77666-116">EXAMPLES</span></span>

### <span data-ttu-id="77666-117">Пример 1: создание концентратора уведомлений</span><span class="sxs-lookup"><span data-stu-id="77666-117">Example 1: Create a notification hub</span></span>
```
PS C:\>New-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configurations\InternalHub.json"
```

<span data-ttu-id="77666-118">Эта команда создает концентратор уведомлений в пространстве имен ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="77666-118">This command creates a notification hub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="77666-119">Новая ступица будет назначена ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="77666-119">The new hub will be assigned to the ContosoNotificationsGroup.</span></span>
<span data-ttu-id="77666-120">Вам не нужно указывать имя или какие-либо другие сведения о конфигурации для концентратора; Эти данные будут взяты из входного файла, C:\Configurations\InternalHub.jsвключены.</span><span class="sxs-lookup"><span data-stu-id="77666-120">You do not need to specify a name or any other configuration information for the hub; that information will be taken from the input file C:\Configurations\InternalHub.json.</span></span>

## <span data-ttu-id="77666-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="77666-121">PARAMETERS</span></span>

### <span data-ttu-id="77666-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77666-122">-DefaultProfile</span></span>
<span data-ttu-id="77666-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="77666-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77666-124">-InputFile</span><span class="sxs-lookup"><span data-stu-id="77666-124">-InputFile</span></span>
<span data-ttu-id="77666-125">Задает путь к файлу JSON, содержащему значения конфигурации для нового концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="77666-125">Specifies the path to a JSON file containing configuration values for the new notification hub.</span></span>

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

### <span data-ttu-id="77666-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="77666-126">-Namespace</span></span>
<span data-ttu-id="77666-127">Задает пространство имен, которому будет назначен Центр уведомлений.</span><span class="sxs-lookup"><span data-stu-id="77666-127">Specifies the namespace to which the notification hub will be assigned.</span></span>
<span data-ttu-id="77666-128">Пространства имен обеспечивают способ группировки и классификации концентраторов уведомлений.</span><span class="sxs-lookup"><span data-stu-id="77666-128">Namespaces provide a way to group and categorize notification hubs.</span></span>
<span data-ttu-id="77666-129">Концентраторы уведомлений должны быть назначены существующему пространству имен.</span><span class="sxs-lookup"><span data-stu-id="77666-129">Notification hubs must be assigned to an existing namespace.</span></span>
<span data-ttu-id="77666-130">Командлет **New-AzNotificationHub** не может создать новое пространство имен.</span><span class="sxs-lookup"><span data-stu-id="77666-130">The **New-AzNotificationHub** cmdlet cannot create a new namespace.</span></span>

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

### <span data-ttu-id="77666-131">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="77666-131">-NotificationHubObj</span></span>
<span data-ttu-id="77666-132">Указывает объект **NotificationHubAttributes** , содержащий сведения о конфигурации для нового концентратора.</span><span class="sxs-lookup"><span data-stu-id="77666-132">Specifies the **NotificationHubAttributes** object that contains configuration information for the new hub.</span></span>

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

### <span data-ttu-id="77666-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="77666-133">-ResourceGroup</span></span>
<span data-ttu-id="77666-134">Указывает группу ресурсов, которой будет назначен концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="77666-134">Specifies the resource group to which the notification hub will be assigned.</span></span>
<span data-ttu-id="77666-135">Группы ресурсов организуют элементы, такие как пространства имен, концентраторы уведомлений и правила авторизации, в целях простого управления запасами и администрирования Azure.</span><span class="sxs-lookup"><span data-stu-id="77666-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>
<span data-ttu-id="77666-136">Необходимо использовать существующую группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="77666-136">You must use an existing resource group.</span></span>
<span data-ttu-id="77666-137">Командлет **New-AzNotificationHub** не может создать новую группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="77666-137">The **New-AzNotificationHub** cmdlet cannot create a new resource group.</span></span>

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

### <span data-ttu-id="77666-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="77666-138">-Confirm</span></span>
<span data-ttu-id="77666-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="77666-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77666-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77666-140">-WhatIf</span></span>
<span data-ttu-id="77666-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="77666-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="77666-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="77666-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77666-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77666-143">CommonParameters</span></span>
<span data-ttu-id="77666-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="77666-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77666-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77666-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77666-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="77666-146">INPUTS</span></span>

### <span data-ttu-id="77666-147">System. String</span><span class="sxs-lookup"><span data-stu-id="77666-147">System.String</span></span>

## <span data-ttu-id="77666-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="77666-148">OUTPUTS</span></span>

### <span data-ttu-id="77666-149">Microsoft. Azure. Commands. NotificationHubs. Models. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="77666-149">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="77666-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="77666-150">NOTES</span></span>

## <span data-ttu-id="77666-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="77666-151">RELATED LINKS</span></span>

[<span data-ttu-id="77666-152">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="77666-152">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="77666-153">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="77666-153">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)

[<span data-ttu-id="77666-154">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="77666-154">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)

