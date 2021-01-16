---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 8EDDA991-55B6-4151-8619-E13E14599ECD
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHub.md
ms.openlocfilehash: 3fb98dc1ef4b13b87fc7cfa41e165d9bc24fc17c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395271"
---
# <span data-ttu-id="d41d0-101">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="d41d0-101">New-AzNotificationHub</span></span>

## <span data-ttu-id="d41d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d41d0-102">SYNOPSIS</span></span>
<span data-ttu-id="d41d0-103">Создает центр уведомлений.</span><span class="sxs-lookup"><span data-stu-id="d41d0-103">Creates a notification hub.</span></span>

## <span data-ttu-id="d41d0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d41d0-104">SYNTAX</span></span>

### <span data-ttu-id="d41d0-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="d41d0-105">InputFileParameterSet</span></span>
```
New-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d41d0-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="d41d0-106">NotificationHubParameterSet</span></span>
```
New-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d41d0-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d41d0-107">DESCRIPTION</span></span>
<span data-ttu-id="d41d0-108">Для создания концентратора уведомлений создается **cmdlet New-AzNotificationHub.**</span><span class="sxs-lookup"><span data-stu-id="d41d0-108">The **New-AzNotificationHub** cmdlet creates a notification hub.</span></span>
<span data-ttu-id="d41d0-109">Концентраторы уведомлений используются для отправки push-уведомлений нескольким клиентам независимо от платформы, используемой этими клиентами.</span><span class="sxs-lookup"><span data-stu-id="d41d0-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="d41d0-110">Концентраторы уведомлений примерно равны отдельным приложениям: в каждом из приложений обычно имеется собственный концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="d41d0-110">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="d41d0-111">Для **создания нового концентратора** уведомлений можно создать два способа.</span><span class="sxs-lookup"><span data-stu-id="d41d0-111">The **New-AzNotificationHub** cmdlet provides two ways to create a new notification hub.</span></span>
<span data-ttu-id="d41d0-112">Вы можете создать экземпляр объекта **NotificationHubAttributes,** а затем настроить его.</span><span class="sxs-lookup"><span data-stu-id="d41d0-112">You can create an instance of the **NotificationHubAttributes** object and then configure that object.</span></span>
<span data-ttu-id="d41d0-113">Затем вы можете скопировать значения этих свойств в новый центр с помощью *параметра NotificationHubObj.*</span><span class="sxs-lookup"><span data-stu-id="d41d0-113">You can then copy those property values to your new hub by through the *NotificationHubObj* parameter.</span></span>
<span data-ttu-id="d41d0-114">Кроме того, можно создать файл нотации объектов JSON (JavaScript), содержащий соответствующие значения конфигурации, а затем применить их с помощью параметра *InputFile.*</span><span class="sxs-lookup"><span data-stu-id="d41d0-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and  then apply those values by using the *InputFile* parameter.</span></span>
<span data-ttu-id="d41d0-115">При использовании в сочетании с **cmdlet New-AzNotificationHub** в предыдущем примере JSON создается центр уведомлений ContosoNotificationHub, расположенный в центре обработки данных в западной части США.</span><span class="sxs-lookup"><span data-stu-id="d41d0-115">When used in conjunction with the **New-AzNotificationHub** cmdlet, the preceding JSON sample creates a notification hub named ContosoNotificationHub located on the West US datacenter.</span></span>

## <span data-ttu-id="d41d0-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d41d0-116">EXAMPLES</span></span>

### <span data-ttu-id="d41d0-117">Пример 1. Создание концентратора уведомлений</span><span class="sxs-lookup"><span data-stu-id="d41d0-117">Example 1: Create a notification hub</span></span>
```
PS C:\>New-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configurations\InternalHub.json"
```

<span data-ttu-id="d41d0-118">Эта команда создает концентратор уведомлений в области имен ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="d41d0-118">This command creates a notification hub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="d41d0-119">Новый центр будет назначен группе ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="d41d0-119">The new hub will be assigned to the ContosoNotificationsGroup.</span></span>
<span data-ttu-id="d41d0-120">Вам не нужно указывать имя или другие сведения конфигурации для концентратора; которые будут взяты из файла ввода, C:\Configurations\InternalHub.js.</span><span class="sxs-lookup"><span data-stu-id="d41d0-120">You do not need to specify a name or any other configuration information for the hub; that information will be taken from the input file C:\Configurations\InternalHub.json.</span></span>

## <span data-ttu-id="d41d0-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d41d0-121">PARAMETERS</span></span>

### <span data-ttu-id="d41d0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d41d0-122">-DefaultProfile</span></span>
<span data-ttu-id="d41d0-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d41d0-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d41d0-124">-InputFile</span><span class="sxs-lookup"><span data-stu-id="d41d0-124">-InputFile</span></span>
<span data-ttu-id="d41d0-125">Путь к JSON-файлу, который содержит значения конфигурации для нового концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="d41d0-125">Specifies the path to a JSON file containing configuration values for the new notification hub.</span></span>

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

### <span data-ttu-id="d41d0-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d41d0-126">-Namespace</span></span>
<span data-ttu-id="d41d0-127">Определяет пространство имен, которому будет назначен концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="d41d0-127">Specifies the namespace to which the notification hub will be assigned.</span></span>
<span data-ttu-id="d41d0-128">Пространства имен предоставляют возможность группировать и классифицировать концентраторы уведомлений.</span><span class="sxs-lookup"><span data-stu-id="d41d0-128">Namespaces provide a way to group and categorize notification hubs.</span></span>
<span data-ttu-id="d41d0-129">Концентраторы уведомлений должны быть назначены существующему пространству имен.</span><span class="sxs-lookup"><span data-stu-id="d41d0-129">Notification hubs must be assigned to an existing namespace.</span></span>
<span data-ttu-id="d41d0-130">Для нового пространства имен не создается новый **cmdlet New-AzNotificationHub.**</span><span class="sxs-lookup"><span data-stu-id="d41d0-130">The **New-AzNotificationHub** cmdlet cannot create a new namespace.</span></span>

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

### <span data-ttu-id="d41d0-131">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="d41d0-131">-NotificationHubObj</span></span>
<span data-ttu-id="d41d0-132">Указывает объект **NotificationHubAttributes,** который содержит сведения о конфигурации для нового концентратора.</span><span class="sxs-lookup"><span data-stu-id="d41d0-132">Specifies the **NotificationHubAttributes** object that contains configuration information for the new hub.</span></span>

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

### <span data-ttu-id="d41d0-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d41d0-133">-ResourceGroup</span></span>
<span data-ttu-id="d41d0-134">Группа ресурсов, которой будет назначен концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="d41d0-134">Specifies the resource group to which the notification hub will be assigned.</span></span>
<span data-ttu-id="d41d0-135">Группы ресурсов упорядочиют такие элементы, как пространства имен, концентраторы уведомлений и правила авторизации, чтобы упрость управление запасами и администрирование Azure.</span><span class="sxs-lookup"><span data-stu-id="d41d0-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>
<span data-ttu-id="d41d0-136">Необходимо использовать существующую группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d41d0-136">You must use an existing resource group.</span></span>
<span data-ttu-id="d41d0-137">Для **этого не удается** создать новую группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d41d0-137">The **New-AzNotificationHub** cmdlet cannot create a new resource group.</span></span>

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

### <span data-ttu-id="d41d0-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d41d0-138">-Confirm</span></span>
<span data-ttu-id="d41d0-139">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d41d0-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d41d0-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d41d0-140">-WhatIf</span></span>
<span data-ttu-id="d41d0-141">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d41d0-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d41d0-142">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d41d0-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d41d0-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d41d0-143">CommonParameters</span></span>
<span data-ttu-id="d41d0-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d41d0-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d41d0-145">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d41d0-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d41d0-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d41d0-146">INPUTS</span></span>

### <span data-ttu-id="d41d0-147">System.String</span><span class="sxs-lookup"><span data-stu-id="d41d0-147">System.String</span></span>

## <span data-ttu-id="d41d0-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d41d0-148">OUTPUTS</span></span>

### <span data-ttu-id="d41d0-149">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="d41d0-149">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="d41d0-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d41d0-150">NOTES</span></span>

## <span data-ttu-id="d41d0-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d41d0-151">RELATED LINKS</span></span>

[<span data-ttu-id="d41d0-152">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="d41d0-152">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="d41d0-153">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="d41d0-153">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)

[<span data-ttu-id="d41d0-154">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="d41d0-154">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)


