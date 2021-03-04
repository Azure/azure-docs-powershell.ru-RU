---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3BA94976-DE88-4F07-9C06-41FEEDE1B829
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/new-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
ms.openlocfilehash: 20a4da67030962a238838247a7dcf137208e56b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951256"
---
# <span data-ttu-id="ae213-101">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="ae213-101">New-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="ae213-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae213-102">SYNOPSIS</span></span>
<span data-ttu-id="ae213-103">Создание пространства имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="ae213-103">Creates a notification hub namespace.</span></span>

## <span data-ttu-id="ae213-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ae213-104">SYNTAX</span></span>

```
New-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ae213-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae213-105">DESCRIPTION</span></span>
<span data-ttu-id="ae213-106">Для создания пространства имен концентратора уведомлений создается **cmdlet New-AzNotificationHubsNamespace.**</span><span class="sxs-lookup"><span data-stu-id="ae213-106">The **New-AzNotificationHubsNamespace** cmdlet creates a notification hub namespace.</span></span>
<span data-ttu-id="ae213-107">Пространства имен — это логические контейнеры, которые помогают организовать концентраторы уведомлений и управлять ими.</span><span class="sxs-lookup"><span data-stu-id="ae213-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="ae213-108">Необходимо иметь хотя бы одно пространство имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="ae213-108">You must have at least one notification hub namespace.</span></span>
<span data-ttu-id="ae213-109">В одном пространстве имен может быть несколько концентраторов.</span><span class="sxs-lookup"><span data-stu-id="ae213-109">A single namespace can house multiple hubs.</span></span>
<span data-ttu-id="ae213-110">Вы можете использовать несколько пространства имен, чтобы упорядочеть концентраторы или предоставить определенным людям разрешение на управление выбранным подмножеством ваших концентраторов.</span><span class="sxs-lookup"><span data-stu-id="ae213-110">You can have multiple namespaces to organize your hubs, or to give specific individuals permission to manage a selected subset of your hubs.</span></span>
<span data-ttu-id="ae213-111">Чтобы создать пространство имен, укажите уникальное имя для пространства имен. указать центр обработки данных, в котором будет расположено пространство имен; и укажите группу ресурсов, которая будет назначена области имен.</span><span class="sxs-lookup"><span data-stu-id="ae213-111">To create a namespace, make sure that you specify a unique name for the namespace; specify the datacenter where the namespace will be located; and, specify the resource group that the namespace will be assigned to.</span></span>
<span data-ttu-id="ae213-112">После создания пространства имен можно использовать New-AzNotificationHubsNamespaceAuthorizationRules для назначения в него правил авторизации.</span><span class="sxs-lookup"><span data-stu-id="ae213-112">After the namespace has been created you can use the New-AzNotificationHubsNamespaceAuthorizationRules cmdlet to assign authorization rules to that namespace.</span></span>
<span data-ttu-id="ae213-113">Правила авторизации используются для управления разрешениями на доступ к области имен.</span><span class="sxs-lookup"><span data-stu-id="ae213-113">Authorization rules are used to manage permissions to the namespace.</span></span>

## <span data-ttu-id="ae213-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ae213-114">EXAMPLES</span></span>

### <span data-ttu-id="ae213-115">Пример 1. Создание концентратора уведомлений</span><span class="sxs-lookup"><span data-stu-id="ae213-115">Example 1: Create a notification hub</span></span>
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners"
```

<span data-ttu-id="ae213-116">Эта команда создает концентратор уведомлений ContosoPartners.</span><span class="sxs-lookup"><span data-stu-id="ae213-116">This command creates a notification hub named ContosoPartners.</span></span>
<span data-ttu-id="ae213-117">Пространство имен будет расположено в центре обработки данных Западной части США и назначено группе ресурсов ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="ae213-117">The namespace will be located in the West US datacenter and be assigned to the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="ae213-118">Пример 2. Создание концентратора уведомлений с тегами</span><span class="sxs-lookup"><span data-stu-id="ae213-118">Example 2: Create a notification hub with tags</span></span>
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners" -Tags @{Name="Audience";Value="PartnerOrganizations"}
```

<span data-ttu-id="ae213-119">Эта команда создает концентратор уведомлений ContosoPartners.</span><span class="sxs-lookup"><span data-stu-id="ae213-119">This command creates a notification hub named ContosoPartners.</span></span>
<span data-ttu-id="ae213-120">Пространство имен будет расположено в центре обработки данных Западной части США и назначено группе ресурсов ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="ae213-120">The namespace will be located in the West US datacenter and be assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="ae213-121">Кроме того, эта команда создает тег с именем Audience и значением PartnerOrganizations и которая назначена области имен.</span><span class="sxs-lookup"><span data-stu-id="ae213-121">In addition, this command creates a tag with the name Audience and the value PartnerOrganizations and is assigned to the namespace.</span></span>
<span data-ttu-id="ae213-122">Это гарантирует, что пространство имен будет отображаться при фильтрации элементов, для которых тегу аудитории назначено имя PartnerOrganizations.</span><span class="sxs-lookup"><span data-stu-id="ae213-122">This ensures that the namespace will be displayed any time you filter for items where the Audience tag is set to PartnerOrganizations.</span></span>

## <span data-ttu-id="ae213-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae213-123">PARAMETERS</span></span>

### <span data-ttu-id="ae213-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae213-124">-DefaultProfile</span></span>
<span data-ttu-id="ae213-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ae213-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae213-126">-Location</span><span class="sxs-lookup"><span data-stu-id="ae213-126">-Location</span></span>
<span data-ttu-id="ae213-127">Указывает отображаемую имя центра обработки данных, в который будет вмечено пространство имен.</span><span class="sxs-lookup"><span data-stu-id="ae213-127">Specifies the display name of the datacenter that will host the Namespace.</span></span>
<span data-ttu-id="ae213-128">Хотя для этого параметра можно установить любое допустимый расположение, для оптимальной работы может потребоваться использовать центр обработки данных, расположенный рядом с большинством пользователей.</span><span class="sxs-lookup"><span data-stu-id="ae213-128">Although you can set this parameter to any valid location, for optimal performance you might want to use a datacenter located near the majority of your users.</span></span>

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

### <span data-ttu-id="ae213-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ae213-129">-Namespace</span></span>
<span data-ttu-id="ae213-130">Указывает имя нового пространства имен.</span><span class="sxs-lookup"><span data-stu-id="ae213-130">Specifies the name of the new namespace.</span></span>
<span data-ttu-id="ae213-131">Пространства имен предоставляют возможность группировать концентраторы уведомлений и классифицировать их.</span><span class="sxs-lookup"><span data-stu-id="ae213-131">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="ae213-132">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ae213-132">-ResourceGroup</span></span>
<span data-ttu-id="ae213-133">Группа ресурсов, которой будет назначено пространство имен.</span><span class="sxs-lookup"><span data-stu-id="ae213-133">Specifies the resource group to which the namespace will be assigned.</span></span>
<span data-ttu-id="ae213-134">Группы ресурсов упорядочиют такие элементы, как пространства имен, концентраторы уведомлений и правила авторизации, чтобы упрость управление запасами и администрирование.</span><span class="sxs-lookup"><span data-stu-id="ae213-134">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and administration.</span></span>

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

### <span data-ttu-id="ae213-135">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="ae213-135">-SkuTier</span></span>
<span data-ttu-id="ae213-136">Уровень SKU пространства имен</span><span class="sxs-lookup"><span data-stu-id="ae213-136">Sku tier of the namespace</span></span>

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

### <span data-ttu-id="ae213-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="ae213-137">-Tag</span></span>
<span data-ttu-id="ae213-138">Определяет пары значений имен, которые можно использовать для классификации и у организовывать элементы Azure.</span><span class="sxs-lookup"><span data-stu-id="ae213-138">Specifies name-value pairs that can be used to categorize and organize Azure items.</span></span>
<span data-ttu-id="ae213-139">Теги работают так же, как ключевые слова, и работают в развертывании.</span><span class="sxs-lookup"><span data-stu-id="ae213-139">Tags function similar to keywords, and operate across a deployment.</span></span>
<span data-ttu-id="ae213-140">Например, при поиске всех элементов с тегом Department:IT поиск возвратит все элементы Azure, которые имеют этот тег, независимо от типа элемента, расположения или группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ae213-140">For example, if you search for all items with the tag Department:IT the search will return all the Azure items that have that tag, regardless of such things as item type, location, or resource group.</span></span>
<span data-ttu-id="ae213-141">Отдельный тег состоит из двух частей: *"Имя"* и (при желании) *"Значение".*</span><span class="sxs-lookup"><span data-stu-id="ae213-141">An individual tag consists of two parts: the *Name* and, optionally, the *Value*.</span></span>
<span data-ttu-id="ae213-142">Например, в отделе Department:IT имя тега — Department, а значение тега — IT.</span><span class="sxs-lookup"><span data-stu-id="ae213-142">For instance, in Department:IT, the tag name is Department and the tag value is IT.</span></span>
<span data-ttu-id="ae213-143">Чтобы добавить тег, используйте синтаксис таблицы с hash примерно так (при этом создается тег CalendarYear:2016).</span><span class="sxs-lookup"><span data-stu-id="ae213-143">To add a tag, use hash table syntax similar to this, which creates the tag CalendarYear:2016:</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae213-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ae213-144">-Confirm</span></span>
<span data-ttu-id="ae213-145">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ae213-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae213-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae213-146">-WhatIf</span></span>
<span data-ttu-id="ae213-147">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae213-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ae213-148">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ae213-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae213-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae213-149">CommonParameters</span></span>
<span data-ttu-id="ae213-150">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae213-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae213-151">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae213-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae213-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ae213-152">INPUTS</span></span>

### <span data-ttu-id="ae213-153">System.String</span><span class="sxs-lookup"><span data-stu-id="ae213-153">System.String</span></span>

### <span data-ttu-id="ae213-154">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="ae213-154">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ae213-155">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ae213-155">OUTPUTS</span></span>

### <span data-ttu-id="ae213-156">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="ae213-156">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="ae213-157">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ae213-157">NOTES</span></span>

## <span data-ttu-id="ae213-158">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ae213-158">RELATED LINKS</span></span>

[<span data-ttu-id="ae213-159">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="ae213-159">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="ae213-160">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="ae213-160">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)

[<span data-ttu-id="ae213-161">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="ae213-161">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


