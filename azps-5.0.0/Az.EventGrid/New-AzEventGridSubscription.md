---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
ms.openlocfilehash: c1eff968bf72c77e6b4e1c2aedfe50459ec3faef
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248704"
---
# <span data-ttu-id="05da4-101">New-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="05da4-101">New-AzEventGridSubscription</span></span>

## <span data-ttu-id="05da4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="05da4-102">SYNOPSIS</span></span>
<span data-ttu-id="05da4-103">Создает новую подписку на событие сетки событий Azure в разделе, ресурсе Azure, подписке Azure или группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="05da4-103">Creates a new Azure Event Grid Event Subscription to a topic, Azure resource, Azure subscription or Resource Group.</span></span>

## <span data-ttu-id="05da4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="05da4-104">SYNTAX</span></span>

### <span data-ttu-id="05da4-105">ResourceGroupNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="05da4-105">ResourceGroupNameParameterSet (Default)</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-ResourceGroupName] <String>] [-EndpointType <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05da4-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="05da4-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-EndpointType <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-SubjectCaseSensitive]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeliverySchema <String>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryTenantId <String>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05da4-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="05da4-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-EndpointType <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-SubjectCaseSensitive]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeliverySchema <String>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryTenantId <String>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05da4-108">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="05da4-108">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-EventSubscriptionName] <String>
 [-Endpoint] <String> [-EndpointType <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05da4-109">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="05da4-109">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-EventSubscriptionName] <String>
 [-Endpoint] <String> [-EndpointType <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05da4-110">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="05da4-110">CustomTopicEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-TopicName] <String> [-EndpointType <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05da4-111">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="05da4-111">DomainEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-DomainName] <String> [-EndpointType <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05da4-112">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="05da4-112">DomainTopicEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-DomainName] <String> -DomainTopicName <String> [-EndpointType <String>]
 [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-SubjectCaseSensitive]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeliverySchema <String>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryTenantId <String>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05da4-113">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="05da4-113">DESCRIPTION</span></span>
<span data-ttu-id="05da4-114">Создайте новую подписку на событие в разделе сетки событий Azure — поддерживаемом ресурсе Azure, подпиской на Azure или группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="05da4-114">Create a new event subscription to an Azure Event Grid topic, a supported Azure resource, an Azure subscription or Resource Group.</span></span>
<span data-ttu-id="05da4-115">Чтобы создать подписку на события для выбранной подписки Azure, укажите имя и конечную точку для события.</span><span class="sxs-lookup"><span data-stu-id="05da4-115">To create an event subscription to the currently selected Azure subscription, specify the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="05da4-116">Чтобы создать подписку на событие для группы ресурсов, укажите имя группы ресурсов в дополнение к имени подписки на событие и конечной точке назначения.</span><span class="sxs-lookup"><span data-stu-id="05da4-116">To create an event subscription to a resource group, specify the resource group name in addition to the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="05da4-117">Чтобы создать подписку на события в разделе сетки событий Azure, укажите название раздела также.</span><span class="sxs-lookup"><span data-stu-id="05da4-117">To create an event subscription to an Azure Event Grid topic, specify the topic name as well.</span></span>
<span data-ttu-id="05da4-118">Чтобы создать подписку на событие для поддерживаемого ресурса Azure, укажите полный ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="05da4-118">To create an event subscription to a supported Azure resource, specify the full resource ID of the resource.</span></span> <span data-ttu-id="05da4-119">Чтобы просмотреть список поддерживаемых типов, выполните командлет Get-AzEventGridTopicType.</span><span class="sxs-lookup"><span data-stu-id="05da4-119">To view the list of supported types, run the Get-AzEventGridTopicType cmdlet.</span></span>

## <span data-ttu-id="05da4-120">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="05da4-120">EXAMPLES</span></span>

### <span data-ttu-id="05da4-121">Пример 1</span><span class="sxs-lookup"><span data-stu-id="05da4-121">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="05da4-122">Создает новую подписку \` на событие EventSubscription1 \` на сетку событий Azure, \` элемент1 \` в группе ресурсов \` MyResourceGroupName \` с конечной точкой веб-перехватчика https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="05da4-122">Creates a new event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="05da4-123">В этой подписке на события используются фильтры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="05da4-123">This event subscription uses default filters.</span></span>

### <span data-ttu-id="05da4-124">Пример 2</span><span class="sxs-lookup"><span data-stu-id="05da4-124">Example 2</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="05da4-125">Создает новую подписку на событие \` EventSubscription1 \` к группе ресурсов \` MyResourceGroupName \` с конечной точкой веб-перехватчика https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="05da4-125">Creates a new event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\` with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="05da4-126">В этой подписке на события используются фильтры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="05da4-126">This event subscription uses default filters.</span></span>

### <span data-ttu-id="05da4-127">Пример 3</span><span class="sxs-lookup"><span data-stu-id="05da4-127">Example 3</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="05da4-128">Создает новую подписку на \` события \` , EventSubscription1 к текущей выбранной подписке Azure с конечной точкой веб-перехватчика https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="05da4-128">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="05da4-129">В этой подписке на события используются фильтры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="05da4-129">This event subscription uses default filters.</span></span>

### <span data-ttu-id="05da4-130">Пример 4</span><span class="sxs-lookup"><span data-stu-id="05da4-130">Example 4</span></span>
```powershell
PS C:\> $includedEventTypes = "Microsoft.Resources.ResourceWriteFailure", "Microsoft.Resources.ResourceWriteSuccess"
PS C:\> $labels = "Finance", "HR"
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1 -SubjectBeginsWith "TestPrefix" -SubjectEndsWith "TestSuffix" -IncludedEventType $includedEventTypes -Label $labels
```

<span data-ttu-id="05da4-131">Создает новую подписку на \` события \` , EventSubscription1 к текущей выбранной подписке Azure с конечной точкой веб-перехватчика https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="05da4-131">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="05da4-132">Эта подписка на события указывает дополнительные фильтры для типов событий и субъектов, и только события, соответствующие этим фильтрам, будут доставляться в конечную точку назначения.</span><span class="sxs-lookup"><span data-stu-id="05da4-132">This event subscription specifies the additional filters for event types and subject, and only events matching those filters will be delivered to the destination endpoint.</span></span>

### <span data-ttu-id="05da4-133">Пример 5</span><span class="sxs-lookup"><span data-stu-id="05da4-133">Example 5</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -EventSubscriptionName EventSubscription1 -EndpointType "eventhub" -Endpoint "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1"
```

<span data-ttu-id="05da4-134">Создает новую подписку на \` событие \` , EventSubscription1 на текущую выбранную подписку Azure с указанным центром событий в качестве места назначения для событий.</span><span class="sxs-lookup"><span data-stu-id="05da4-134">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the specified event hub as the destination for events.</span></span> <span data-ttu-id="05da4-135">В этой подписке на события используются фильтры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="05da4-135">This event subscription uses default filters.</span></span>

### <span data-ttu-id="05da4-136">Пример 6</span><span class="sxs-lookup"><span data-stu-id="05da4-136">Example 6</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="05da4-137">Создает новую подписку на событие, \` EventSubscription1 \` с заданной конечной точкой веб-перехватчика в пространстве имен EventHub https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="05da4-137">Creates a new event subscription \`EventSubscription1\` to an EventHub namespace with the specified webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="05da4-138">В этой подписке на события используются фильтры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="05da4-138">This event subscription uses default filters.</span></span>

## <span data-ttu-id="05da4-139">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="05da4-139">PARAMETERS</span></span>

### <span data-ttu-id="05da4-140">-AdvancedFilter</span><span class="sxs-lookup"><span data-stu-id="05da4-140">-AdvancedFilter</span></span>
<span data-ttu-id="05da4-141">Расширенный фильтр, указывающий массив из нескольких значений Hashtable, которые используются для фильтрации на основе атрибутов.</span><span class="sxs-lookup"><span data-stu-id="05da4-141">Advanced filter that specifies an array of multiple Hashtable values that are used for the attribute-based filtering.</span></span> <span data-ttu-id="05da4-142">У каждого значения Hashtable есть следующие ключи: сведения об операции, ключе, значении или значениях.</span><span class="sxs-lookup"><span data-stu-id="05da4-142">Each Hashtable value has the following keys-value info: Operation, Key and Value or Values.</span></span> <span data-ttu-id="05da4-143">Может принимать одно из следующих значений: Number in, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringNotIn, StringBeginsWith или StringEndsWith.</span><span class="sxs-lookup"><span data-stu-id="05da4-143">Operator can be one of the following values: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith or StringContains.</span></span> <span data-ttu-id="05da4-144">Key представляет свойство полезных данных, к которому применяются дополнительные политики фильтрации.</span><span class="sxs-lookup"><span data-stu-id="05da4-144">Key represents the payload property where the advanced filtering policies are applied.</span></span> <span data-ttu-id="05da4-145">Наконец, значение или значения представляют значение или набор значений, которые должны быть сопоставлены.</span><span class="sxs-lookup"><span data-stu-id="05da4-145">Finally, Value or Values represent the value or set of values to be matched.</span></span> <span data-ttu-id="05da4-146">Это может быть одно значение соответствующего типа или массива значений.</span><span class="sxs-lookup"><span data-stu-id="05da4-146">This can be a single value of the corresponding type or an array of values.</span></span> <span data-ttu-id="05da4-147">В качестве примера параметров расширенного фильтра: $AdvancedFilters = @ ($AdvFilter 1, $AdvFilter 2), где $AdvFilter 1 = @ {operator = "Number in"; Key = "Data. key1"; Значения = @ (1; 2)} и $AdvFilter 2 = @ {operator = "StringBringsWith"; Key = "Тема"; Значения = @ ("SubjectPrefix1"; "SubjectPrefix2")}</span><span class="sxs-lookup"><span data-stu-id="05da4-147">As an example of the advanced filter parameters: $AdvancedFilters=@($AdvFilter1, $AdvFilter2) where $AdvFilter1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} and $AdvFilter2=@{operator="StringBringsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05da4-148">-AzureActiveDirectoryApplicationIdOrUri</span><span class="sxs-lookup"><span data-stu-id="05da4-148">-AzureActiveDirectoryApplicationIdOrUri</span></span>
<span data-ttu-id="05da4-149">Идентификатор приложения Azure Active Directory (AAD) или URI для получения маркера доступа, который будет включен в качестве маркера носителя в запросах на доставку. Применимо только для веб-перехватчика в качестве назначения.</span><span class="sxs-lookup"><span data-stu-id="05da4-149">The Azure Active Directory (AAD) Application Id or Uri to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases: AliasAadAppIdUri

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases: AliasAadAppIdUri

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05da4-150">-AzureActiveDirectoryTenantId</span><span class="sxs-lookup"><span data-stu-id="05da4-150">-AzureActiveDirectoryTenantId</span></span>
<span data-ttu-id="05da4-151">Идентификатор клиента Azure Active Directory (AAD) для получения маркера доступа, который будет включен в качестве маркера носителя в запросах на доставку. Применимо только для веб-перехватчика в качестве назначения.</span><span class="sxs-lookup"><span data-stu-id="05da4-151">The Azure Active Directory (AAD) Tenant Id to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases: AliasAadTenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases: AliasAadTenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05da4-152">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="05da4-152">-DeadLetterEndpoint</span></span>
<span data-ttu-id="05da4-153">Конечная точка, используемая для хранения событий, не проданных доставку.</span><span class="sxs-lookup"><span data-stu-id="05da4-153">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="05da4-154">Укажите идентификатор ресурса Azure контейнера BLOB-объектов хранилища.</span><span class="sxs-lookup"><span data-stu-id="05da4-154">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="05da4-155">Например:/Subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span><span class="sxs-lookup"><span data-stu-id="05da4-155">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05da4-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05da4-156">-DefaultProfile</span></span>
<span data-ttu-id="05da4-157">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="05da4-157">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="05da4-158">-DeliverySchema</span><span class="sxs-lookup"><span data-stu-id="05da4-158">-DeliverySchema</span></span>
<span data-ttu-id="05da4-159">Схема, используемая при доставке событий в назначение.</span><span class="sxs-lookup"><span data-stu-id="05da4-159">The schema to be used when delivering events to the destination.</span></span> <span data-ttu-id="05da4-160">Возможные значения: eventgridschema, CustomInputSchema или cloudeventv01schema.</span><span class="sxs-lookup"><span data-stu-id="05da4-160">The possible values are: eventgridschema, CustomInputSchema, or cloudeventv01schema.</span></span> <span data-ttu-id="05da4-161">Значение по умолчанию — CustomInputSchema.</span><span class="sxs-lookup"><span data-stu-id="05da4-161">Default value is CustomInputSchema.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:
Accepted values: EventGridSchema, CustomInputSchema, CloudEventSchemaV1_0

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:
Accepted values: EventGridSchema, CustomInputSchema, CloudEventSchemaV1_0

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05da4-162">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="05da4-162">-DomainInputObject</span></span>
<span data-ttu-id="05da4-163">Объект Domain EventGrid.</span><span class="sxs-lookup"><span data-stu-id="05da4-163">EventGrid Domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: EventSubscriptionDomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05da4-164">-ИмяДомена</span><span class="sxs-lookup"><span data-stu-id="05da4-164">-DomainName</span></span>
<span data-ttu-id="05da4-165">Имя домена сетки событий, для которого нужно создать подписку на события.</span><span class="sxs-lookup"><span data-stu-id="05da4-165">The name of the Event Grid domain to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05da4-166">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="05da4-166">-DomainTopicInputObject</span></span>
<span data-ttu-id="05da4-167">Объект темы домена EventGrid.</span><span class="sxs-lookup"><span data-stu-id="05da4-167">EventGrid Domain Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic
Parameter Sets: EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05da4-168">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="05da4-168">-DomainTopicName</span></span>
<span data-ttu-id="05da4-169">Имя домена, для которого требуется создать подписку на события.</span><span class="sxs-lookup"><span data-stu-id="05da4-169">The name of the domain topic to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05da4-170">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="05da4-170">-Endpoint</span></span>
<span data-ttu-id="05da4-171">Конечная точка подписки на события.</span><span class="sxs-lookup"><span data-stu-id="05da4-171">Event subscription destination endpoint.</span></span>
<span data-ttu-id="05da4-172">Это может быть URL-адрес веб-перехватчика или идентификатор ресурса Azure EventHub, очередь хранилища, hybridconnection или servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="05da4-172">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="05da4-173">Например, идентификатор ресурса для гибридного подключения имеет следующий вид:/Subscriptions/[ИД подписки Azure]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="05da4-173">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="05da4-174">Предполагается, что конечная точка должна быть создана и доступна для использования перед выполнением каких бы то ни было командлетов сетки событий.</span><span class="sxs-lookup"><span data-stu-id="05da4-174">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>


```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05da4-175">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="05da4-175">-EndpointType</span></span>
<span data-ttu-id="05da4-176">Тип конечной точки.</span><span class="sxs-lookup"><span data-stu-id="05da4-176">Endpoint Type.</span></span>
<span data-ttu-id="05da4-177">Это может быть веб-перехватчик, eventhub, storagequeue, hybridconnection или servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="05da4-177">This can be webhook, eventhub, storagequeue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="05da4-178">Значением по умолчанию является веб-перехватчик.</span><span class="sxs-lookup"><span data-stu-id="05da4-178">Default value is webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue, servicebustopic, azurefunction

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue, servicebustopic, azurefunction

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05da4-179">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="05da4-179">-EventSubscriptionName</span></span>
<span data-ttu-id="05da4-180">Имя подписки на события</span><span class="sxs-lookup"><span data-stu-id="05da4-180">The name of the event subscription</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05da4-181">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="05da4-181">-EventTtl</span></span>
<span data-ttu-id="05da4-182">Время доставки события (в минутах).</span><span class="sxs-lookup"><span data-stu-id="05da4-182">The time in minutes for the event delivery.</span></span> <span data-ttu-id="05da4-183">Это значение должно находиться в диапазоне от 1 до 1440</span><span class="sxs-lookup"><span data-stu-id="05da4-183">This value must be between 1 and 1440</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05da4-184">-ExpirationDate</span><span class="sxs-lookup"><span data-stu-id="05da4-184">-ExpirationDate</span></span>
<span data-ttu-id="05da4-185">Определяет дату и время окончания срока действия для подписки на события, после которого подписку на события будут аннулированы.</span><span class="sxs-lookup"><span data-stu-id="05da4-185">Determines the expiration DateTime for the event subscription after which event subscription will retire.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05da4-186">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="05da4-186">-IncludedEventType</span></span>
<span data-ttu-id="05da4-187">Фильтр, который задает список типов событий для включения. Если не указано, будут включены все типы событий.</span><span class="sxs-lookup"><span data-stu-id="05da4-187">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05da4-188">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05da4-188">-InputObject</span></span>
<span data-ttu-id="05da4-189">Объект темы EventGrid.</span><span class="sxs-lookup"><span data-stu-id="05da4-189">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="05da4-190">-Label</span><span class="sxs-lookup"><span data-stu-id="05da4-190">-Label</span></span>
<span data-ttu-id="05da4-191">Метки для подписки на события</span><span class="sxs-lookup"><span data-stu-id="05da4-191">Labels for the event subscription</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05da4-192">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="05da4-192">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="05da4-193">Максимальное количество попыток доставки события.</span><span class="sxs-lookup"><span data-stu-id="05da4-193">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="05da4-194">Это значение должно быть в диапазоне от 1 до 30</span><span class="sxs-lookup"><span data-stu-id="05da4-194">This value must be between 1 and 30</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05da4-195">-MaxEventsPerBatch</span><span class="sxs-lookup"><span data-stu-id="05da4-195">-MaxEventsPerBatch</span></span>
<span data-ttu-id="05da4-196">Максимальное количество событий в пакете.</span><span class="sxs-lookup"><span data-stu-id="05da4-196">The maximum number of events in a batch.</span></span> <span data-ttu-id="05da4-197">Это значение должно находиться в диапазоне от 1 до 5000.</span><span class="sxs-lookup"><span data-stu-id="05da4-197">This value must be between 1 and 5000.</span></span> <span data-ttu-id="05da4-198">Этот параметр является допустимым только в том случае, если тип Endpint — только веб-перехватчик.</span><span class="sxs-lookup"><span data-stu-id="05da4-198">This parameter is valid when Endpint Type is webhook only.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05da4-199">-PreferredBatchSizeInKiloBytes</span><span class="sxs-lookup"><span data-stu-id="05da4-199">-PreferredBatchSizeInKiloBytes</span></span>
<span data-ttu-id="05da4-200">Предпочтительный размер пакета в килобайтах.</span><span class="sxs-lookup"><span data-stu-id="05da4-200">The preferred batch size in kilobytes.</span></span> <span data-ttu-id="05da4-201">Это значение должно находиться в диапазоне от 1 до 1024.</span><span class="sxs-lookup"><span data-stu-id="05da4-201">This value must be between 1 and 1024.</span></span> <span data-ttu-id="05da4-202">Этот параметр является допустимым только в том случае, если тип Endpint — только веб-перехватчик.</span><span class="sxs-lookup"><span data-stu-id="05da4-202">This parameter is valid when Endpint Type is webhook only.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05da4-203">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05da4-203">-ResourceGroupName</span></span>
<span data-ttu-id="05da4-204">Группа ресурсов для темы.</span><span class="sxs-lookup"><span data-stu-id="05da4-204">The resource group of the topic.</span></span>

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
Parameter Sets: CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05da4-205">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="05da4-205">-ResourceId</span></span>
<span data-ttu-id="05da4-206">Идентификатор ресурса, для которого требуется создать подписку на событие.</span><span class="sxs-lookup"><span data-stu-id="05da4-206">The identifier of the resource to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="05da4-207">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="05da4-207">-SubjectBeginsWith</span></span>
<span data-ttu-id="05da4-208">Фильтр, указывающий на то, что будут включены только события, соответствующие указанному префиксу темы.</span><span class="sxs-lookup"><span data-stu-id="05da4-208">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="05da4-209">Если не указано, будут включены события со всеми префиксами субъектов.</span><span class="sxs-lookup"><span data-stu-id="05da4-209">If not specified, events with all subject prefixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05da4-210">-SubjectCaseSensitive</span><span class="sxs-lookup"><span data-stu-id="05da4-210">-SubjectCaseSensitive</span></span>
<span data-ttu-id="05da4-211">Фильтр, указывающий, что поле темы должно сравниваться с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="05da4-211">Filter that specifies that the subject field should be compared in a case sensitive manner.</span></span>
<span data-ttu-id="05da4-212">Если не указано, тема будет сравниваться без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="05da4-212">If not specified, subject will be compared in a case insensitive manner.</span></span>

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

### <span data-ttu-id="05da4-213">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="05da4-213">-SubjectEndsWith</span></span>
<span data-ttu-id="05da4-214">Фильтр, указывающий, что в него будут включены только события, соответствующие указанному суффиксу темы.</span><span class="sxs-lookup"><span data-stu-id="05da4-214">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="05da4-215">Если не указано, будут включены события со всеми суффиксами тем.</span><span class="sxs-lookup"><span data-stu-id="05da4-215">If not specified, events with all subject suffixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05da4-216">-TopicName</span><span class="sxs-lookup"><span data-stu-id="05da4-216">-TopicName</span></span>
<span data-ttu-id="05da4-217">Название темы, на которую следует создать подписку на событие.</span><span class="sxs-lookup"><span data-stu-id="05da4-217">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="05da4-218">-Confirm</span><span class="sxs-lookup"><span data-stu-id="05da4-218">-Confirm</span></span>
<span data-ttu-id="05da4-219">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="05da4-219">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05da4-220">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05da4-220">-WhatIf</span></span>
<span data-ttu-id="05da4-221">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="05da4-221">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05da4-222">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="05da4-222">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05da4-223">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05da4-223">CommonParameters</span></span>
<span data-ttu-id="05da4-224">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="05da4-224">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05da4-225">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="05da4-225">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05da4-226">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="05da4-226">INPUTS</span></span>

### <span data-ttu-id="05da4-227">System. String</span><span class="sxs-lookup"><span data-stu-id="05da4-227">System.String</span></span>

### <span data-ttu-id="05da4-228">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="05da4-228">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="05da4-229">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="05da4-229">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="05da4-230">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="05da4-230">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="05da4-231">System. String []</span><span class="sxs-lookup"><span data-stu-id="05da4-231">System.String[]</span></span>

### <span data-ttu-id="05da4-232">System. Int32</span><span class="sxs-lookup"><span data-stu-id="05da4-232">System.Int32</span></span>

## <span data-ttu-id="05da4-233">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="05da4-233">OUTPUTS</span></span>

### <span data-ttu-id="05da4-234">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="05da4-234">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="05da4-235">Пуск</span><span class="sxs-lookup"><span data-stu-id="05da4-235">NOTES</span></span>

## <span data-ttu-id="05da4-236">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="05da4-236">RELATED LINKS</span></span>
