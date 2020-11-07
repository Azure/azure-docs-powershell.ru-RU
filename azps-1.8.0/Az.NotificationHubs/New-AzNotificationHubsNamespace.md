---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3BA94976-DE88-4F07-9C06-41FEEDE1B829
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
ms.openlocfilehash: a9675f2473488d1415a83ae0454a3841cd10d589
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729899"
---
# <span data-ttu-id="39b9c-101">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="39b9c-101">New-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="39b9c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="39b9c-102">SYNOPSIS</span></span>
<span data-ttu-id="39b9c-103">Создает пространство имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="39b9c-103">Creates a notification hub namespace.</span></span>

## <span data-ttu-id="39b9c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="39b9c-104">SYNTAX</span></span>

```
New-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="39b9c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="39b9c-105">DESCRIPTION</span></span>
<span data-ttu-id="39b9c-106">Командлет **New-AzNotificationHubsNamespace** создает пространство имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="39b9c-106">The **New-AzNotificationHubsNamespace** cmdlet creates a notification hub namespace.</span></span>
<span data-ttu-id="39b9c-107">Пространства имен — это логические контейнеры, помогающие упорядочивать концентраторы уведомлений и управлять ими.</span><span class="sxs-lookup"><span data-stu-id="39b9c-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="39b9c-108">Необходимо иметь по крайней мере одно пространство имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="39b9c-108">You must have at least one notification hub namespace.</span></span>
<span data-ttu-id="39b9c-109">Одно пространство имен может быть размещено на нескольких ступицах.</span><span class="sxs-lookup"><span data-stu-id="39b9c-109">A single namespace can house multiple hubs.</span></span>
<span data-ttu-id="39b9c-110">Вы можете использовать несколько пространств имен для Организации концентраторов или предоставить определенным пользователям разрешение на управление выбранной подмножеством концентраторов.</span><span class="sxs-lookup"><span data-stu-id="39b9c-110">You can have multiple namespaces to organize your hubs, or to give specific individuals permission to manage a selected subset of your hubs.</span></span>
<span data-ttu-id="39b9c-111">Чтобы создать пространство имен, убедитесь, что вы указали уникальное имя для пространства имен. Укажите центр обработки данных, в котором будет находиться пространство имен; Укажите группу ресурсов, которой будет назначено пространство имен.</span><span class="sxs-lookup"><span data-stu-id="39b9c-111">To create a namespace, make sure that you specify a unique name for the namespace; specify the datacenter where the namespace will be located; and, specify the resource group that the namespace will be assigned to.</span></span>
<span data-ttu-id="39b9c-112">После создания пространства имен можно использовать командлет New-AzNotificationHubsNamespaceAuthorizationRules для назначения правил авторизации этому пространству имен.</span><span class="sxs-lookup"><span data-stu-id="39b9c-112">After the namespace has been created you can use the New-AzNotificationHubsNamespaceAuthorizationRules cmdlet to assign authorization rules to that namespace.</span></span>
<span data-ttu-id="39b9c-113">Правила авторизации используются для управления разрешениями пространства имен.</span><span class="sxs-lookup"><span data-stu-id="39b9c-113">Authorization rules are used to manage permissions to the namespace.</span></span>

## <span data-ttu-id="39b9c-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="39b9c-114">EXAMPLES</span></span>

### <span data-ttu-id="39b9c-115">Пример 1: создание концентратора уведомлений</span><span class="sxs-lookup"><span data-stu-id="39b9c-115">Example 1: Create a notification hub</span></span>
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners"
```

<span data-ttu-id="39b9c-116">Эта команда создает концентратор уведомлений с именем ContosoPartners.</span><span class="sxs-lookup"><span data-stu-id="39b9c-116">This command creates a notification hub named ContosoPartners.</span></span>
<span data-ttu-id="39b9c-117">Пространство имен будет находиться в центре обработки данных "Западная часть США" и назначено группе ресурсов ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="39b9c-117">The namespace will be located in the West US datacenter and be assigned to the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="39b9c-118">Пример 2: создание концентратора уведомлений с помощью тегов</span><span class="sxs-lookup"><span data-stu-id="39b9c-118">Example 2: Create a notification hub with tags</span></span>
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners" -Tags @{Name="Audience";Value="PartnerOrganizations"}
```

<span data-ttu-id="39b9c-119">Эта команда создает концентратор уведомлений с именем ContosoPartners.</span><span class="sxs-lookup"><span data-stu-id="39b9c-119">This command creates a notification hub named ContosoPartners.</span></span>
<span data-ttu-id="39b9c-120">Пространство имен будет находиться в центре обработки данных "Западная часть США" и назначено группе ресурсов ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="39b9c-120">The namespace will be located in the West US datacenter and be assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="39b9c-121">Кроме того, эта команда создает тег с именем аудитории и значением PartnerOrganizations и назначается пространству имен.</span><span class="sxs-lookup"><span data-stu-id="39b9c-121">In addition, this command creates a tag with the name Audience and the value PartnerOrganizations and is assigned to the namespace.</span></span>
<span data-ttu-id="39b9c-122">Это гарантирует, что во время фильтрации для элементов, в которых тег аудитории имеет значение PartnerOrganizations, будет отображаться пространство имен.</span><span class="sxs-lookup"><span data-stu-id="39b9c-122">This ensures that the namespace will be displayed any time you filter for items where the Audience tag is set to PartnerOrganizations.</span></span>

## <span data-ttu-id="39b9c-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="39b9c-123">PARAMETERS</span></span>

### <span data-ttu-id="39b9c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39b9c-124">-DefaultProfile</span></span>
<span data-ttu-id="39b9c-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="39b9c-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="39b9c-126">-Location</span><span class="sxs-lookup"><span data-stu-id="39b9c-126">-Location</span></span>
<span data-ttu-id="39b9c-127">Указывает отображаемое имя центра обработки данных, на котором будет размещено пространство имен.</span><span class="sxs-lookup"><span data-stu-id="39b9c-127">Specifies the display name of the datacenter that will host the Namespace.</span></span>
<span data-ttu-id="39b9c-128">Несмотря на то, что вы можете установить для этого параметра любое допустимое расположение, для оптимальной производительности может потребоваться центр обработки данных, находящийся рядом с большинством пользователей.</span><span class="sxs-lookup"><span data-stu-id="39b9c-128">Although you can set this parameter to any valid location, for optimal performance you might want to use a datacenter located near the majority of your users.</span></span>

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

### <span data-ttu-id="39b9c-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="39b9c-129">-Namespace</span></span>
<span data-ttu-id="39b9c-130">Указывает имя нового пространства имен.</span><span class="sxs-lookup"><span data-stu-id="39b9c-130">Specifies the name of the new namespace.</span></span>
<span data-ttu-id="39b9c-131">Пространства имен обеспечивают способ группировки и классификации концентраторов уведомлений.</span><span class="sxs-lookup"><span data-stu-id="39b9c-131">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="39b9c-132">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="39b9c-132">-ResourceGroup</span></span>
<span data-ttu-id="39b9c-133">Указывает группу ресурсов, которой будет назначено пространство имен.</span><span class="sxs-lookup"><span data-stu-id="39b9c-133">Specifies the resource group to which the namespace will be assigned.</span></span>
<span data-ttu-id="39b9c-134">Группы ресурсов организуют элементы, такие как пространства имен, концентраторы уведомлений и правила авторизации, таким образом, чтобы упростить управление запасами и администрирование.</span><span class="sxs-lookup"><span data-stu-id="39b9c-134">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and administration.</span></span>

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

### <span data-ttu-id="39b9c-135">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="39b9c-135">-SkuTier</span></span>
<span data-ttu-id="39b9c-136">Уровень SKU пространства имен</span><span class="sxs-lookup"><span data-stu-id="39b9c-136">Sku tier of the namespace</span></span>

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

### <span data-ttu-id="39b9c-137">-Тег</span><span class="sxs-lookup"><span data-stu-id="39b9c-137">-Tag</span></span>
<span data-ttu-id="39b9c-138">Указывает пары "имя-значение", которые можно использовать для классификации и упорядочения элементов Azure.</span><span class="sxs-lookup"><span data-stu-id="39b9c-138">Specifies name-value pairs that can be used to categorize and organize Azure items.</span></span>
<span data-ttu-id="39b9c-139">Теги похожи на ключевые слова и работают в рамках развертывания.</span><span class="sxs-lookup"><span data-stu-id="39b9c-139">Tags function similar to keywords, and operate across a deployment.</span></span>
<span data-ttu-id="39b9c-140">Например, если вы ищете все элементы в отделе тегов: поиск вернет все элементы Azure с таким тегом, независимо от того, как тип элемента, расположение или группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="39b9c-140">For example, if you search for all items with the tag Department:IT the search will return all the Azure items that have that tag, regardless of such things as item type, location, or resource group.</span></span>
<span data-ttu-id="39b9c-141">Отдельный тег состоит из двух частей: *имени* и, при необходимости, *значения*.</span><span class="sxs-lookup"><span data-stu-id="39b9c-141">An individual tag consists of two parts: the *Name* and, optionally, the *Value*.</span></span>
<span data-ttu-id="39b9c-142">Например, в отделе: имя тега — "Отдел", а значение тега —.</span><span class="sxs-lookup"><span data-stu-id="39b9c-142">For instance, in Department:IT, the tag name is Department and the tag value is IT.</span></span>
<span data-ttu-id="39b9c-143">Чтобы добавить тег, используйте синтаксис хэш-таблицы, аналогичный приведенному ниже, который создает тег CalendarYear: 2016:</span><span class="sxs-lookup"><span data-stu-id="39b9c-143">To add a tag, use hash table syntax similar to this, which creates the tag CalendarYear:2016:</span></span>

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

### <span data-ttu-id="39b9c-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="39b9c-144">-Confirm</span></span>
<span data-ttu-id="39b9c-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="39b9c-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39b9c-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39b9c-146">-WhatIf</span></span>
<span data-ttu-id="39b9c-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="39b9c-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="39b9c-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="39b9c-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39b9c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39b9c-149">CommonParameters</span></span>
<span data-ttu-id="39b9c-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="39b9c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39b9c-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39b9c-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39b9c-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="39b9c-152">INPUTS</span></span>

### <span data-ttu-id="39b9c-153">System. String</span><span class="sxs-lookup"><span data-stu-id="39b9c-153">System.String</span></span>

### <span data-ttu-id="39b9c-154">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="39b9c-154">System.Collections.Hashtable</span></span>

## <span data-ttu-id="39b9c-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="39b9c-155">OUTPUTS</span></span>

### <span data-ttu-id="39b9c-156">Microsoft. Azure. Commands. NotificationHubs. Models. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="39b9c-156">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="39b9c-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="39b9c-157">NOTES</span></span>

## <span data-ttu-id="39b9c-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="39b9c-158">RELATED LINKS</span></span>

[<span data-ttu-id="39b9c-159">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="39b9c-159">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="39b9c-160">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="39b9c-160">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)

[<span data-ttu-id="39b9c-161">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="39b9c-161">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


