---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
ms.openlocfilehash: 1c0391fa266e498c717bc4eb43bd92ab93be508f
ms.sourcegitcommit: 7aaa37edc9681b643946505bcbc3cc6435f1d7ca
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "94395192"
---
# <span data-ttu-id="155f6-101">New-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="155f6-101">New-AzEventGridSubscription</span></span>

## <span data-ttu-id="155f6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="155f6-102">SYNOPSIS</span></span>
<span data-ttu-id="155f6-103">Создает новую подписку на событие сетки событий Azure в разделе, ресурсе Azure, подписке Azure или группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="155f6-103">Creates a new Azure Event Grid Event Subscription to a topic, Azure resource, Azure subscription or Resource Group.</span></span>

## <span data-ttu-id="155f6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="155f6-104">SYNTAX</span></span>

### <span data-ttu-id="155f6-105">ResourceGroupNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="155f6-105">ResourceGroupNameParameterSet (Default)</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-ResourceGroupName] <String>] [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="155f6-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="155f6-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="155f6-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="155f6-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="155f6-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="155f6-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-TopicName] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="155f6-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="155f6-109">DESCRIPTION</span></span>
<span data-ttu-id="155f6-110">Создайте новую подписку на событие в разделе сетки событий Azure — поддерживаемом ресурсе Azure, подпиской на Azure или группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="155f6-110">Create a new event subscription to an Azure Event Grid topic, a supported Azure resource, an Azure subscription or Resource Group.</span></span>
<span data-ttu-id="155f6-111">Чтобы создать подписку на события для выбранной подписки Azure, укажите имя и конечную точку для события.</span><span class="sxs-lookup"><span data-stu-id="155f6-111">To create an event subscription to the currently selected Azure subscription, specify the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="155f6-112">Чтобы создать подписку на событие для группы ресурсов, укажите имя группы ресурсов в дополнение к имени подписки на событие и конечной точке назначения.</span><span class="sxs-lookup"><span data-stu-id="155f6-112">To create an event subscription to a resource group, specify the resource group name in addition to the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="155f6-113">Чтобы создать подписку на события в разделе сетки событий Azure, укажите название раздела также.</span><span class="sxs-lookup"><span data-stu-id="155f6-113">To create an event subscription to an Azure Event Grid topic, specify the topic name as well.</span></span>
<span data-ttu-id="155f6-114">Чтобы создать подписку на событие для поддерживаемого ресурса Azure, укажите полный ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="155f6-114">To create an event subscription to a supported Azure resource, specify the full resource ID of the resource.</span></span> <span data-ttu-id="155f6-115">Чтобы просмотреть список поддерживаемых типов, выполните командлет Get-AzEventGridTopicType.</span><span class="sxs-lookup"><span data-stu-id="155f6-115">To view the list of supported types, run the Get-AzEventGridTopicType cmdlet.</span></span>

## <span data-ttu-id="155f6-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="155f6-116">EXAMPLES</span></span>

### <span data-ttu-id="155f6-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="155f6-117">Example 1</span></span>
```
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="155f6-118">Создает новую подписку \` на событие EventSubscription1 \` на сетку событий Azure, \` элемент1 \` в группе ресурсов \` MyResourceGroupName \` с конечной точкой веб-перехватчика `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="155f6-118">Creates a new event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="155f6-119">В этой подписке на события используются фильтры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="155f6-119">This event subscription uses default filters.</span></span>

### <span data-ttu-id="155f6-120">Пример 2</span><span class="sxs-lookup"><span data-stu-id="155f6-120">Example 2</span></span>
```
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="155f6-121">Создает новую подписку на событие \` EventSubscription1 \` к группе ресурсов \` MyResourceGroupName \` с конечной точкой веб-перехватчика `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="155f6-121">Creates a new event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\` with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="155f6-122">В этой подписке на события используются фильтры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="155f6-122">This event subscription uses default filters.</span></span>

### <span data-ttu-id="155f6-123">Пример 3</span><span class="sxs-lookup"><span data-stu-id="155f6-123">Example 3</span></span>
```
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="155f6-124">Создает новую подписку на \` события \` , EventSubscription1 к текущей выбранной подписке Azure с конечной точкой веб-перехватчика `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="155f6-124">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="155f6-125">В этой подписке на события используются фильтры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="155f6-125">This event subscription uses default filters.</span></span>

### <span data-ttu-id="155f6-126">Пример 4</span><span class="sxs-lookup"><span data-stu-id="155f6-126">Example 4</span></span>
```
PS C:\> $includedEventTypes = "Microsoft.Resources.ResourceWriteFailure", "Microsoft.Resources.ResourceWriteSuccess"
PS C:\> $labels = "Finance", "HR"
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1 -SubjectBeginsWith "TestPrefix" -SubjectEndsWith "TestSuffix" -IncludedEventType $includedEventTypes -Label $labels
```

<span data-ttu-id="155f6-127">Создает новую подписку на \` события \` , EventSubscription1 к текущей выбранной подписке Azure с конечной точкой веб-перехватчика `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="155f6-127">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="155f6-128">Эта подписка на события указывает дополнительные фильтры для типов событий и субъектов, и только события, соответствующие этим фильтрам, будут доставляться в конечную точку назначения.</span><span class="sxs-lookup"><span data-stu-id="155f6-128">This event subscription specifies the additional filters for event types and subject, and only events matching those filters will be delivered to the destination endpoint.</span></span>

### <span data-ttu-id="155f6-129">Пример 5</span><span class="sxs-lookup"><span data-stu-id="155f6-129">Example 5</span></span>
```
PS C:\> New-AzEventGridSubscription -EventSubscriptionName EventSubscription1 -EndpointType "eventhub" -Endpoint "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1"
```

<span data-ttu-id="155f6-130">Создает новую подписку на \` событие \` , EventSubscription1 на текущую выбранную подписку Azure с указанным центром событий в качестве места назначения для событий.</span><span class="sxs-lookup"><span data-stu-id="155f6-130">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the specified event hub as the destination for events.</span></span> <span data-ttu-id="155f6-131">В этой подписке на события используются фильтры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="155f6-131">This event subscription uses default filters.</span></span>

### <span data-ttu-id="155f6-132">Пример 6</span><span class="sxs-lookup"><span data-stu-id="155f6-132">Example 6</span></span>
```
PS C:\> New-AzEventGridSubscription -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="155f6-133">Создает новую подписку на событие, \` EventSubscription1 \` с заданной конечной точкой веб-перехватчика в пространстве имен EventHub `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="155f6-133">Creates a new event subscription \`EventSubscription1\` to an EventHub namespace with the specified webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="155f6-134">В этой подписке на события используются фильтры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="155f6-134">This event subscription uses default filters.</span></span>

## <span data-ttu-id="155f6-135">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="155f6-135">PARAMETERS</span></span>

### <span data-ttu-id="155f6-136">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="155f6-136">-DeadLetterEndpoint</span></span>
<span data-ttu-id="155f6-137">Конечная точка, используемая для хранения событий, не проданных доставку.</span><span class="sxs-lookup"><span data-stu-id="155f6-137">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="155f6-138">Укажите идентификатор ресурса Azure контейнера BLOB-объектов хранилища.</span><span class="sxs-lookup"><span data-stu-id="155f6-138">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="155f6-139">Например:/Subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span><span class="sxs-lookup"><span data-stu-id="155f6-139">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="155f6-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="155f6-140">-DefaultProfile</span></span>
<span data-ttu-id="155f6-141">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="155f6-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="155f6-142">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="155f6-142">-Endpoint</span></span>
<span data-ttu-id="155f6-143">Конечная точка подписки на события.</span><span class="sxs-lookup"><span data-stu-id="155f6-143">Event subscription destination endpoint.</span></span>
<span data-ttu-id="155f6-144">Это может быть URL-адрес веб-перехватчика или идентификатор ресурса Azure для EventHub, очереди хранения или hybridconnection.</span><span class="sxs-lookup"><span data-stu-id="155f6-144">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue or hybridconnection.</span></span> <span data-ttu-id="155f6-145">Например, идентификатор ресурса для гибридного подключения имеет следующий вид:/Subscriptions/[ИД подписки Azure]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="155f6-145">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="155f6-146">Предполагается, что конечная точка должна быть создана и доступна для использования перед выполнением каких бы то ни было командлетов сетки событий.</span><span class="sxs-lookup"><span data-stu-id="155f6-146">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>


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
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="155f6-147">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="155f6-147">-EndpointType</span></span>
<span data-ttu-id="155f6-148">Тип конечной точки.</span><span class="sxs-lookup"><span data-stu-id="155f6-148">Endpoint Type.</span></span>
<span data-ttu-id="155f6-149">Это может быть веб-перехватчик, eventhub, storagequeue или hybridconnection.</span><span class="sxs-lookup"><span data-stu-id="155f6-149">This can be webhook, eventhub, storagequeue, or hybridconnection.</span></span> <span data-ttu-id="155f6-150">Значением по умолчанию является веб-перехватчик.</span><span class="sxs-lookup"><span data-stu-id="155f6-150">Default value is webhook.</span></span>


```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="155f6-151">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="155f6-151">-EventSubscriptionName</span></span>
<span data-ttu-id="155f6-152">Имя подписки на события</span><span class="sxs-lookup"><span data-stu-id="155f6-152">The name of the event subscription</span></span>

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
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="155f6-153">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="155f6-153">-EventTtl</span></span>
<span data-ttu-id="155f6-154">Время доставки события (в минутах).</span><span class="sxs-lookup"><span data-stu-id="155f6-154">The time in minutes for the event delivery.</span></span> <span data-ttu-id="155f6-155">Это значение должно находиться в диапазоне от 1 до 1440</span><span class="sxs-lookup"><span data-stu-id="155f6-155">This value must be between 1 and 1440</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="155f6-156">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="155f6-156">-IncludedEventType</span></span>
<span data-ttu-id="155f6-157">Фильтр, который задает список типов событий для включения. Если не указано, будут включены все типы событий.</span><span class="sxs-lookup"><span data-stu-id="155f6-157">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

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
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="155f6-158">-InputObject</span><span class="sxs-lookup"><span data-stu-id="155f6-158">-InputObject</span></span>
<span data-ttu-id="155f6-159">Объект темы EventGrid.</span><span class="sxs-lookup"><span data-stu-id="155f6-159">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="155f6-160">-Label</span><span class="sxs-lookup"><span data-stu-id="155f6-160">-Label</span></span>
<span data-ttu-id="155f6-161">Метки для подписки на события</span><span class="sxs-lookup"><span data-stu-id="155f6-161">Labels for the event subscription</span></span>

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
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="155f6-162">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="155f6-162">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="155f6-163">Максимальное количество попыток доставки события.</span><span class="sxs-lookup"><span data-stu-id="155f6-163">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="155f6-164">Это значение должно быть в диапазоне от 1 до 30</span><span class="sxs-lookup"><span data-stu-id="155f6-164">This value must be between 1 and 30</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="155f6-165">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="155f6-165">-ResourceGroupName</span></span>
<span data-ttu-id="155f6-166">Группа ресурсов для темы.</span><span class="sxs-lookup"><span data-stu-id="155f6-166">The resource group of the topic.</span></span>

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

### <span data-ttu-id="155f6-167">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="155f6-167">-ResourceId</span></span>
<span data-ttu-id="155f6-168">Идентификатор ресурса, для которого требуется создать подписку на событие.</span><span class="sxs-lookup"><span data-stu-id="155f6-168">The identifier of the resource to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="155f6-169">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="155f6-169">-SubjectBeginsWith</span></span>
<span data-ttu-id="155f6-170">Фильтр, указывающий на то, что будут включены только события, соответствующие указанному префиксу темы.</span><span class="sxs-lookup"><span data-stu-id="155f6-170">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="155f6-171">Если не указано, будут включены события со всеми префиксами субъектов.</span><span class="sxs-lookup"><span data-stu-id="155f6-171">If not specified, events with all subject prefixes will be included.</span></span>

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
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="155f6-172">-SubjectCaseSensitive</span><span class="sxs-lookup"><span data-stu-id="155f6-172">-SubjectCaseSensitive</span></span>
<span data-ttu-id="155f6-173">Фильтр, указывающий, что поле темы должно сравниваться с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="155f6-173">Filter that specifies that the subject field should be compared in a case sensitive manner.</span></span>
<span data-ttu-id="155f6-174">Если не указано, тема будет сравниваться без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="155f6-174">If not specified, subject will be compared in a case insensitive manner.</span></span>

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

### <span data-ttu-id="155f6-175">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="155f6-175">-SubjectEndsWith</span></span>
<span data-ttu-id="155f6-176">Фильтр, указывающий, что в него будут включены только события, соответствующие указанному суффиксу темы.</span><span class="sxs-lookup"><span data-stu-id="155f6-176">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="155f6-177">Если не указано, будут включены события со всеми суффиксами тем.</span><span class="sxs-lookup"><span data-stu-id="155f6-177">If not specified, events with all subject suffixes will be included.</span></span>

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
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="155f6-178">-TopicName</span><span class="sxs-lookup"><span data-stu-id="155f6-178">-TopicName</span></span>
<span data-ttu-id="155f6-179">Название темы, на которую следует создать подписку на событие.</span><span class="sxs-lookup"><span data-stu-id="155f6-179">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="155f6-180">-Confirm</span><span class="sxs-lookup"><span data-stu-id="155f6-180">-Confirm</span></span>
<span data-ttu-id="155f6-181">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="155f6-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="155f6-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="155f6-182">-WhatIf</span></span>
<span data-ttu-id="155f6-183">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="155f6-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="155f6-184">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="155f6-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="155f6-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="155f6-185">CommonParameters</span></span>
<span data-ttu-id="155f6-186">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="155f6-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="155f6-187">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="155f6-187">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="155f6-188">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="155f6-188">INPUTS</span></span>

### <span data-ttu-id="155f6-189">System. String</span><span class="sxs-lookup"><span data-stu-id="155f6-189">System.String</span></span>

### <span data-ttu-id="155f6-190">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="155f6-190">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="155f6-191">System. String []</span><span class="sxs-lookup"><span data-stu-id="155f6-191">System.String[]</span></span>

## <span data-ttu-id="155f6-192">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="155f6-192">OUTPUTS</span></span>

### <span data-ttu-id="155f6-193">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="155f6-193">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="155f6-194">Пуск</span><span class="sxs-lookup"><span data-stu-id="155f6-194">NOTES</span></span>

## <span data-ttu-id="155f6-195">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="155f6-195">RELATED LINKS</span></span>
