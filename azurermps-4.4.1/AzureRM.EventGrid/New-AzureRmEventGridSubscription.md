---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridSubscription.md
ms.openlocfilehash: ed2855571ccd3ce10a8a41fd72f5e14fde7bba16
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569527"
---
# <span data-ttu-id="77e4e-101">New-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="77e4e-101">New-AzureRmEventGridSubscription</span></span>

## <span data-ttu-id="77e4e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="77e4e-102">SYNOPSIS</span></span>
<span data-ttu-id="77e4e-103">Создает новую подписку на событие сетки событий Azure в разделе, ресурсе Azure, подписке Azure или группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="77e4e-103">Creates a new Azure Event Grid Event Subscription to a topic, Azure resource, Azure subscription or Resource Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77e4e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="77e4e-104">SYNTAX</span></span>

### <span data-ttu-id="77e4e-105">ResourceGroupNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="77e4e-105">ResourceGroupNameParameterSet (Default)</span></span>
```
New-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-ResourceGroupName] <String>] [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77e4e-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="77e4e-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzureRmEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77e4e-107">EventSubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="77e4e-107">EventSubscriptionInputObjectSet</span></span>
```
New-AzureRmEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String>
 [-Endpoint] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77e4e-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="77e4e-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
New-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-TopicName] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77e4e-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="77e4e-109">DESCRIPTION</span></span>
<span data-ttu-id="77e4e-110">Создайте новую подписку на событие в разделе сетки событий Azure — поддерживаемом ресурсе Azure, подпиской на Azure или группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="77e4e-110">Create a new event subscription to an Azure Event Grid topic, a supported Azure resource, an Azure subscription or Resource Group.</span></span>
<span data-ttu-id="77e4e-111">Чтобы создать подписку на события для выбранной подписки Azure, укажите имя и конечную точку для события.</span><span class="sxs-lookup"><span data-stu-id="77e4e-111">To create an event subscription to the currently selected Azure subscription, specify the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="77e4e-112">Чтобы создать подписку на событие для группы ресурсов, укажите имя группы ресурсов в дополнение к имени подписки на событие и конечной точке назначения.</span><span class="sxs-lookup"><span data-stu-id="77e4e-112">To create an event subscription to a resource group, specify the resource group name in addition to the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="77e4e-113">Чтобы создать подписку на события в разделе сетки событий Azure, укажите название раздела также.</span><span class="sxs-lookup"><span data-stu-id="77e4e-113">To create an event subscription to an Azure Event Grid topic, specify the topic name as well.</span></span>
<span data-ttu-id="77e4e-114">Чтобы создать подписку на событие для поддерживаемого ресурса Azure, укажите полный ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="77e4e-114">To create an event subscription to a supported Azure resource, specify the full resource ID of the resource.</span></span> <span data-ttu-id="77e4e-115">Чтобы просмотреть список поддерживаемых типов, выполните командлет Get-AzureRmEventGridTopicType.</span><span class="sxs-lookup"><span data-stu-id="77e4e-115">To view the list of supported types, run the Get-AzureRmEventGridTopicType cmdlet.</span></span>

## <span data-ttu-id="77e4e-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="77e4e-116">EXAMPLES</span></span>

### <span data-ttu-id="77e4e-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="77e4e-117">Example 1</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="77e4e-118">Создает новую подписку \` на событие EventSubscription1 \` на сетку событий Azure, \` элемент1 \` в группе ресурсов \` MyResourceGroupName \` с конечной точкой веб-перехватчика https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="77e4e-118">Creates a new event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="77e4e-119">В этой подписке на события используются фильтры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="77e4e-119">This event subscription uses default filters.</span></span>

### <span data-ttu-id="77e4e-120">Пример 2</span><span class="sxs-lookup"><span data-stu-id="77e4e-120">Example 2</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="77e4e-121">Создает новую подписку на событие \` EventSubscription1 \` к группе ресурсов \` MyResourceGroupName \` с конечной точкой веб-перехватчика https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="77e4e-121">Creates a new event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\` with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="77e4e-122">В этой подписке на события используются фильтры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="77e4e-122">This event subscription uses default filters.</span></span>

### <span data-ttu-id="77e4e-123">Пример 3</span><span class="sxs-lookup"><span data-stu-id="77e4e-123">Example 3</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="77e4e-124">Создает новую подписку на \` события \` , EventSubscription1 к текущей выбранной подписке Azure с конечной точкой веб-перехватчика https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="77e4e-124">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="77e4e-125">В этой подписке на события используются фильтры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="77e4e-125">This event subscription uses default filters.</span></span>

### <span data-ttu-id="77e4e-126">Пример 4</span><span class="sxs-lookup"><span data-stu-id="77e4e-126">Example 4</span></span>
```
PS C:\> $includedEventTypes = "Microsoft.Resources.ResourceWriteFailure", "Microsoft.Resources.ResourceWriteSuccess"
PS C:\> $labels = "Finance", "HR"
PS C:\> New-AzureRmEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1 -SubjectBeginsWith "TestPrefix" -SubjectEndsWith "TestSuffix" -IncludedEventType $includedEventTypes -Label $labels
```

<span data-ttu-id="77e4e-127">Создает новую подписку на \` события \` , EventSubscription1 к текущей выбранной подписке Azure с конечной точкой веб-перехватчика https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="77e4e-127">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="77e4e-128">Эта подписка на события указывает дополнительные фильтры для типов событий и субъектов, и только события, соответствующие этим фильтрам, будут доставляться в конечную точку назначения.</span><span class="sxs-lookup"><span data-stu-id="77e4e-128">This event subscription specifies the additional filters for event types and subject, and only events matching those filters will be delivered to the destination endpoint.</span></span>

### <span data-ttu-id="77e4e-129">Пример 5</span><span class="sxs-lookup"><span data-stu-id="77e4e-129">Example 5</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1 -EndpointType "eventhub" -Endpoint "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1"
```

<span data-ttu-id="77e4e-130">Создает новую подписку на \` событие \` , EventSubscription1 на текущую выбранную подписку Azure с указанным центром событий в качестве места назначения для событий.</span><span class="sxs-lookup"><span data-stu-id="77e4e-130">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the specified event hub as the destination for events.</span></span> <span data-ttu-id="77e4e-131">В этой подписке на события используются фильтры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="77e4e-131">This event subscription uses default filters.</span></span>

### <span data-ttu-id="77e4e-132">Пример 6</span><span class="sxs-lookup"><span data-stu-id="77e4e-132">Example 6</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1" -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="77e4e-133">Создает новую подписку \` на событие EventSubscription1 \` в пространство имен EventHub с указанной конечной точкой webhhok https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="77e4e-133">Creates a new event subscription \`EventSubscription1\` to an EventHub namespace with the specified webhhok destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="77e4e-134">В этой подписке на события используются фильтры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="77e4e-134">This event subscription uses default filters.</span></span>

## <span data-ttu-id="77e4e-135">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="77e4e-135">PARAMETERS</span></span>

### <span data-ttu-id="77e4e-136">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="77e4e-136">-Endpoint</span></span>
<span data-ttu-id="77e4e-137">Конечная точка подписки на события.</span><span class="sxs-lookup"><span data-stu-id="77e4e-137">Event subscription destination endpoint.</span></span>
<span data-ttu-id="77e4e-138">Это может быть URL-адрес веб-перехватчика или идентификатор ресурса Azure EventHub.</span><span class="sxs-lookup"><span data-stu-id="77e4e-138">This can be a webhook URL or the Azure resource ID of an EventHub.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77e4e-139">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="77e4e-139">-EndpointType</span></span>
<span data-ttu-id="77e4e-140">Тип конечной точки.</span><span class="sxs-lookup"><span data-stu-id="77e4e-140">Endpoint Type.</span></span>
<span data-ttu-id="77e4e-141">Это может быть веб-перехватчик или eventhub</span><span class="sxs-lookup"><span data-stu-id="77e4e-141">This can be webhook or eventhub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 
Accepted values: webhook, eventhub, webhook, eventhub

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 
Accepted values: webhook, eventhub, webhook, eventhub

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77e4e-142">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="77e4e-142">-EventSubscriptionName</span></span>
<span data-ttu-id="77e4e-143">Имя подписки на события</span><span class="sxs-lookup"><span data-stu-id="77e4e-143">The name of the event subscription</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77e4e-144">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="77e4e-144">-IncludedEventType</span></span>
<span data-ttu-id="77e4e-145">Фильтр, который задает список типов событий для включения. Если не указано, будут включены все типы событий.</span><span class="sxs-lookup"><span data-stu-id="77e4e-145">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77e4e-146">-InputObject</span><span class="sxs-lookup"><span data-stu-id="77e4e-146">-InputObject</span></span>
<span data-ttu-id="77e4e-147">Объект темы EventGrid.</span><span class="sxs-lookup"><span data-stu-id="77e4e-147">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77e4e-148">-Label</span><span class="sxs-lookup"><span data-stu-id="77e4e-148">-Label</span></span>
<span data-ttu-id="77e4e-149">Метки для подписки на события</span><span class="sxs-lookup"><span data-stu-id="77e4e-149">Labels for the event subscription</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77e4e-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77e4e-150">-ResourceGroupName</span></span>
<span data-ttu-id="77e4e-151">Группа ресурсов для темы.</span><span class="sxs-lookup"><span data-stu-id="77e4e-151">The resource group of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77e4e-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77e4e-152">-ResourceId</span></span>
<span data-ttu-id="77e4e-153">Идентификатор ресурса, для которого требуется создать подписку на событие.</span><span class="sxs-lookup"><span data-stu-id="77e4e-153">The identifier of the resource to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77e4e-154">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="77e4e-154">-SubjectBeginsWith</span></span>
<span data-ttu-id="77e4e-155">Фильтр, указывающий на то, что будут включены только события, соответствующие указанному префиксу темы.</span><span class="sxs-lookup"><span data-stu-id="77e4e-155">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="77e4e-156">Если не указано, будут включены события со всеми префиксами субъектов.</span><span class="sxs-lookup"><span data-stu-id="77e4e-156">If not specified, events with all subject prefixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77e4e-157">-SubjectCaseSensitive</span><span class="sxs-lookup"><span data-stu-id="77e4e-157">-SubjectCaseSensitive</span></span>
<span data-ttu-id="77e4e-158">Фильтр, указывающий, что поле темы должно сравниваться с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="77e4e-158">Filter that specifies that the subject field should be compared in a case sensitive manner.</span></span>
<span data-ttu-id="77e4e-159">Если не указано, тема будет сравниваться без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="77e4e-159">If not specified, subject will be compared in a case insensitive manner.</span></span>

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

### <span data-ttu-id="77e4e-160">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="77e4e-160">-SubjectEndsWith</span></span>
<span data-ttu-id="77e4e-161">Фильтр, указывающий, что в него будут включены только события, соответствующие указанному суффиксу темы.</span><span class="sxs-lookup"><span data-stu-id="77e4e-161">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="77e4e-162">Если не указано, будут включены события со всеми суффиксами тем.</span><span class="sxs-lookup"><span data-stu-id="77e4e-162">If not specified, events with all subject suffixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77e4e-163">-TopicName</span><span class="sxs-lookup"><span data-stu-id="77e4e-163">-TopicName</span></span>
<span data-ttu-id="77e4e-164">Название темы, на которую следует создать подписку на событие.</span><span class="sxs-lookup"><span data-stu-id="77e4e-164">The name of the topic to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77e4e-165">-Confirm</span><span class="sxs-lookup"><span data-stu-id="77e4e-165">-Confirm</span></span>
<span data-ttu-id="77e4e-166">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="77e4e-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77e4e-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77e4e-167">-WhatIf</span></span>
<span data-ttu-id="77e4e-168">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="77e4e-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77e4e-169">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="77e4e-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77e4e-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77e4e-170">-DefaultProfile</span></span>
<span data-ttu-id="77e4e-171">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="77e4e-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77e4e-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77e4e-172">CommonParameters</span></span>
<span data-ttu-id="77e4e-173">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="77e4e-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77e4e-174">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77e4e-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77e4e-175">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="77e4e-175">INPUTS</span></span>

### <span data-ttu-id="77e4e-176">System. String</span><span class="sxs-lookup"><span data-stu-id="77e4e-176">System.String</span></span>
<span data-ttu-id="77e4e-177">Microsoft. Azure. Commands. EventGrid. Models. PSTopic System. Management. Automation. SwitchParameter System. String []</span><span class="sxs-lookup"><span data-stu-id="77e4e-177">Microsoft.Azure.Commands.EventGrid.Models.PSTopic System.Management.Automation.SwitchParameter System.String[]</span></span>

## <span data-ttu-id="77e4e-178">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="77e4e-178">OUTPUTS</span></span>

### <span data-ttu-id="77e4e-179">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="77e4e-179">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="77e4e-180">Пуск</span><span class="sxs-lookup"><span data-stu-id="77e4e-180">NOTES</span></span>

## <span data-ttu-id="77e4e-181">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="77e4e-181">RELATED LINKS</span></span>

