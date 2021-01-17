---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 1B2AA717-ECD6-4CC0-AB6D-A199AF21A4A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
ms.openlocfilehash: c367c4b4f7ebe7c9d6d51b832eed22249f262864
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98425076"
---
# <span data-ttu-id="0de68-101">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="0de68-101">Set-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="0de68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0de68-102">SYNOPSIS</span></span>
<span data-ttu-id="0de68-103">Задает значения свойств для пространства имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="0de68-103">Sets property values for a notification hub namespace.</span></span>

## <span data-ttu-id="0de68-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0de68-104">SYNTAX</span></span>

```
Set-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-State] <NamespaceState>] [[-Critical] <Boolean>] [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0de68-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0de68-105">DESCRIPTION</span></span>
<span data-ttu-id="0de68-106">Для свойства существующего пространства имен концентратора уведомлений задаются значения свойств **set-AzNotificationHubsNamespace.**</span><span class="sxs-lookup"><span data-stu-id="0de68-106">The **Set-AzNotificationHubsNamespace** cmdlet sets the property values of an existing notification hub namespace.</span></span>
<span data-ttu-id="0de68-107">Пространства имен — это логические контейнеры, которые помогают организовать концентраторы уведомлений и управлять ими.</span><span class="sxs-lookup"><span data-stu-id="0de68-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="0de68-108">Необходимо иметь хотя бы одно пространство имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="0de68-108">You must have at least one notification hub namespace.</span></span>
<span data-ttu-id="0de68-109">Кроме того, у всех концентраторов уведомлений должно быть назначено пространство имен.</span><span class="sxs-lookup"><span data-stu-id="0de68-109">Additionally, all notification hubs must have an assigned namespace.</span></span>
<span data-ttu-id="0de68-110">Этот cmdlet в основном используется для того, чтобы включить и отключить пространство имен.</span><span class="sxs-lookup"><span data-stu-id="0de68-110">This cmdlet is primarily used to enable and disable a namespace.</span></span>
<span data-ttu-id="0de68-111">Если пространство имен отключено, пользователи не могут подключаться к концентраторам уведомлений в этом пространстве и администраторы не могут использовать их для отправки push-уведомлений.</span><span class="sxs-lookup"><span data-stu-id="0de68-111">When a namespace is disabled, users cannot connect to any of the notification hubs in the namespace, nor can administrators use those hubs to send push notifications.</span></span>
<span data-ttu-id="0de68-112">Чтобы снова включить отключенное пространство имен, с помощью этого cmdlet можно установить для свойства **State** пространства имен состояние Active (Состояние) области имен.</span><span class="sxs-lookup"><span data-stu-id="0de68-112">To re-enable a disabled namespace, use this cmdlet to set the **State** property of the namespace to Active.</span></span>
<span data-ttu-id="0de68-113">С помощью этого командлета можно также пометить пространство имен как важное.</span><span class="sxs-lookup"><span data-stu-id="0de68-113">You can also use this cmdlet to tag a namespace as critical.</span></span>
<span data-ttu-id="0de68-114">Это предотвращает удаление пространства имен.</span><span class="sxs-lookup"><span data-stu-id="0de68-114">This prevents the namespace from being deleted.</span></span>
<span data-ttu-id="0de68-115">Чтобы удалить критическое пространство имен, сначала необходимо удалить критический тег.</span><span class="sxs-lookup"><span data-stu-id="0de68-115">To remove a critical namespace you must first remove the Critical tag.</span></span>

## <span data-ttu-id="0de68-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0de68-116">EXAMPLES</span></span>

### <span data-ttu-id="0de68-117">Пример 1. Отключение пространства имен</span><span class="sxs-lookup"><span data-stu-id="0de68-117">Example 1: Disable a namespace</span></span>
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Disabled"
```

<span data-ttu-id="0de68-118">Эта команда отключает пространство имен "ContosoPartners", расположенное в центре обработки данных "Запад США", и назначено группе ресурсов ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="0de68-118">This command disables the namespace named ContosoPartners located in the West US datacenter and assigned to the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="0de68-119">Пример 2. Включить пространство имен</span><span class="sxs-lookup"><span data-stu-id="0de68-119">Example 2: Enable a namespace</span></span>
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Active"
```

<span data-ttu-id="0de68-120">Эта команда включает пространство имен ContosoPartners в центре обработки данных "Запад. США" и назначено группе ресурсов ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="0de68-120">This command enables the namespace named ContosoPartners located in the West US datacenter and assigned to the ContosoNotificationsGroup resource group.</span></span>

## <span data-ttu-id="0de68-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0de68-121">PARAMETERS</span></span>

### <span data-ttu-id="0de68-122">-Критическое</span><span class="sxs-lookup"><span data-stu-id="0de68-122">-Critical</span></span>
<span data-ttu-id="0de68-123">Указывает, является ли пространство имен критическим.</span><span class="sxs-lookup"><span data-stu-id="0de68-123">Indicates whether the namespace is a critical namespace.</span></span>
<span data-ttu-id="0de68-124">Критически важные области имен удалить нельзя.</span><span class="sxs-lookup"><span data-stu-id="0de68-124">Critical namespaces cannot be deleted.</span></span>
<span data-ttu-id="0de68-125">Чтобы удалить критическое пространство имен, необходимо указать для этого свойства значение False, чтобы пометить его как некритическое.</span><span class="sxs-lookup"><span data-stu-id="0de68-125">To delete a critical namespace, you must set the value of this property to False in order to mark the namespace as non-critical.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0de68-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0de68-126">-DefaultProfile</span></span>
<span data-ttu-id="0de68-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0de68-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0de68-128">-Force</span><span class="sxs-lookup"><span data-stu-id="0de68-128">-Force</span></span>
<span data-ttu-id="0de68-129">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="0de68-129">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0de68-130">-Location</span><span class="sxs-lookup"><span data-stu-id="0de68-130">-Location</span></span>
<span data-ttu-id="0de68-131">Указывает отображаемого имя центра обработки данных, на котором размещено пространство имен.</span><span class="sxs-lookup"><span data-stu-id="0de68-131">Specifies the display name of the datacenter that hosts the namespace.</span></span>
<span data-ttu-id="0de68-132">Хотя для этого параметра можно установить любое допустимый расположение Azure, для оптимальной работы следует использовать центр обработки данных, расположенный рядом с большинством пользователей.</span><span class="sxs-lookup"><span data-stu-id="0de68-132">Although you can set this parameter to any valid Azure location, for optimal performance you should use a datacenter located near the majority of your users.</span></span>
<span data-ttu-id="0de68-133">Чтобы получить список местоположений Azure, запустите следующую команду: `Get-AzLocation | Select-Object DisplayName`</span><span class="sxs-lookup"><span data-stu-id="0de68-133">To get an up-to-date list of Azure locations run the following command: `Get-AzLocation | Select-Object DisplayName`</span></span>

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

### <span data-ttu-id="0de68-134">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0de68-134">-Namespace</span></span>
<span data-ttu-id="0de68-135">Определяет пространство имен, которое изменяет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0de68-135">Specifies the namespace that this cmdlet modifies.</span></span>
<span data-ttu-id="0de68-136">Пространства имен предоставляют возможность группировать и классифицировать концентраторы уведомлений.</span><span class="sxs-lookup"><span data-stu-id="0de68-136">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="0de68-137">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0de68-137">-ResourceGroup</span></span>
<span data-ttu-id="0de68-138">Группа ресурсов, которой назначено пространство имен.</span><span class="sxs-lookup"><span data-stu-id="0de68-138">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="0de68-139">Группы ресурсов упорядочиют такие элементы, как пространства имен, концентраторы уведомлений и правила авторизации, чтобы упрость управление запасами и администрирование Azure.</span><span class="sxs-lookup"><span data-stu-id="0de68-139">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="0de68-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="0de68-140">-SkuTier</span></span>
<span data-ttu-id="0de68-141">Уровень SKU пространства имен</span><span class="sxs-lookup"><span data-stu-id="0de68-141">Sku tier of the namespace</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0de68-142">-State</span><span class="sxs-lookup"><span data-stu-id="0de68-142">-State</span></span>
<span data-ttu-id="0de68-143">Определяет текущее состояние пространства имен.</span><span class="sxs-lookup"><span data-stu-id="0de68-143">Specifies the current state of the namespace.</span></span>
<span data-ttu-id="0de68-144">Допустимые значения этого параметра: активные и отключенные.</span><span class="sxs-lookup"><span data-stu-id="0de68-144">The acceptable values for this parameter are: Active and Disabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0de68-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="0de68-145">-Tag</span></span>
<span data-ttu-id="0de68-146">Определяет пары "имя-значение", которые можно использовать для классификации и у организовывать элементы Azure.</span><span class="sxs-lookup"><span data-stu-id="0de68-146">Specifies name-value pairs that can be used to categorize and organize Azure items.</span></span>
<span data-ttu-id="0de68-147">Теги работают так же, как ключевые слова, и работают в развертывании.</span><span class="sxs-lookup"><span data-stu-id="0de68-147">Tags function similar to keywords, and operate across a deployment.</span></span>
<span data-ttu-id="0de68-148">Например, при поиске всех элементов с тегом Department:IT поиск возвратит все элементы Azure, которые имеют этот тег, независимо от типа элемента, расположения или группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0de68-148">For example, if you search for all items with the tag Department:IT the search will return all the Azure items that have that tag, regardless of such things as item type, location, or resource group.</span></span>
<span data-ttu-id="0de68-149">Отдельный тег состоит из двух частей: *имя* и (необязательно) *значение.*</span><span class="sxs-lookup"><span data-stu-id="0de68-149">An individual tag consists of two parts: the *Name* and (optionally) the *Value*.</span></span>
<span data-ttu-id="0de68-150">Например, в отделе Department:IT имя тега — "Отдел", а значением тега — ИТ.</span><span class="sxs-lookup"><span data-stu-id="0de68-150">For example, in Department:IT, the tag name is Department and the tag value is IT.</span></span>
<span data-ttu-id="0de68-151">Чтобы добавить тег, используйте синтаксис таблицы с hash similar to this (создание тега CalendarYear:2016: -Tags @{Name="CalendarYear"); Value="2016"} Чтобы добавить несколько тегов в одной команде, разделите отдельные теги запятой: -Tag @{Name="CalendarYear"; Value="2016"}, @{Name="FiscalYear"; Value="2017"}</span><span class="sxs-lookup"><span data-stu-id="0de68-151">To add a tag, use hash table syntax similar to this, which creates the tag CalendarYear:2016: -Tags @{Name="CalendarYear";Value="2016"} To add multiple tags in the same command, separate the individual tags by using commas: -Tag @{Name="CalendarYear";Value="2016"}, @{Name="FiscalYear";Value="2017"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0de68-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0de68-152">-Confirm</span></span>
<span data-ttu-id="0de68-153">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0de68-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0de68-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0de68-154">-WhatIf</span></span>
<span data-ttu-id="0de68-155">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0de68-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0de68-156">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0de68-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0de68-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0de68-157">CommonParameters</span></span>
<span data-ttu-id="0de68-158">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0de68-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0de68-159">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0de68-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0de68-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0de68-160">INPUTS</span></span>

### <span data-ttu-id="0de68-161">System.String</span><span class="sxs-lookup"><span data-stu-id="0de68-161">System.String</span></span>

### <span data-ttu-id="0de68-162">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState</span><span class="sxs-lookup"><span data-stu-id="0de68-162">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState</span></span>

### <span data-ttu-id="0de68-163">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0de68-163">System.Boolean</span></span>

### <span data-ttu-id="0de68-164">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="0de68-164">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0de68-165">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0de68-165">OUTPUTS</span></span>

### <span data-ttu-id="0de68-166">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="0de68-166">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="0de68-167">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0de68-167">NOTES</span></span>

## <span data-ttu-id="0de68-168">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0de68-168">RELATED LINKS</span></span>

[<span data-ttu-id="0de68-169">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="0de68-169">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="0de68-170">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="0de68-170">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="0de68-171">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="0de68-171">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)


